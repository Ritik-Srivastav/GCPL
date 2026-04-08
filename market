const MarketBreadthCard = ({
  advancing = null,
  declining = null,
  ratio = null,
}) => {
  // Calculate percentage for the progress bar width
  const total = advancing + declining;
  const advancingWidth = (advancing / total) * 100;

  return (
    <div className="w-auto rounded-2xl border border-cyan-200/20 bg-gradient-to-br from-[#101A2B] via-[#0A1222] to-[#070D18] px-4 py-3 text-white shadow-[0_8px_30px_rgba(0,0,0,0.45)]">
      {/* Title */}
      <p className="text-[13px] font-medium tracking-[0.06em] text-slate-300/90 uppercase">
        Market Breadth
      </p>

      {/* Stats Grid */}
      <div className="mt-3 grid grid-cols-2 gap-4">
        <div>
          <h3 className="text-[30px] font-semibold leading-none text-[#00D084]">
            {advancing}
          </h3>
          <p className="mt-1 text-[12px] font-medium text-slate-400">
            Advancing
          </p>
        </div>
        <div className="text-right">
          <h3 className="text-[30px] font-semibold leading-none text-[#FF0000]">
            {declining}
          </h3>
          <p className="mt-1 text-[12px] font-medium text-slate-400">
            Declining
          </p>
        </div>
      </div>

      {/* Split Progress Bar */}
      <div className="mt-4 flex h-2.5 w-full overflow-hidden rounded-full bg-slate-800">
        <div
          className="h-full bg-[#00D084] transition-all duration-500"
          style={{ width: `${advancingWidth}%` }}
        />
        <div
          className="h-full bg-[#FF0000] transition-all duration-500"
          style={{ width: `${100 - advancingWidth}%` }}
        />
      </div>

      {/* Footer / Ratio */}
      <div className="mt-4 flex justify-between items-center">
        <span className="text-[13px] font-medium text-slate-300">
          A/D Ratio
        </span>
        <span className="text-[13px] font-bold text-[#00D084]">{ratio}</span>
      </div>
    </div>
  );
};

export default MarketBreadthCard;
