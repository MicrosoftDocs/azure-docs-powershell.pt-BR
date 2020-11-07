---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945976"
---
# <span data-ttu-id="e0c7f-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0c7f-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="e0c7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c7f-103">Cria um plano de recuperação de site na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="e0c7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0c7f-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0c7f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c7f-106">O cmdlet **New-AzureSiteRecoveryRecoveryPlan** cria um plano de recuperação no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="e0c7f-107">Um plano de recuperação reúne máquinas virtuais em um grupo para fins de failover e recuperação.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="e0c7f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0c7f-108">EXAMPLES</span></span>

### <span data-ttu-id="e0c7f-109">Exemplo 1: adicionar um plano de recuperação a um cofre de recuperação de site</span><span class="sxs-lookup"><span data-stu-id="e0c7f-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="e0c7f-110">Esse comando adiciona o plano de recuperação chamado RecoveryPlan.xml ao cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e0c7f-111">OS</span><span class="sxs-lookup"><span data-stu-id="e0c7f-111">PARAMETERS</span></span>

### <span data-ttu-id="e0c7f-112">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="e0c7f-112">-File</span></span>
<span data-ttu-id="e0c7f-113">Especifica o caminho do arquivo de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-113">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c7f-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e0c7f-114">-Profile</span></span>
<span data-ttu-id="e0c7f-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0c7f-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c7f-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e0c7f-117">-WaitForCompletion</span></span>
<span data-ttu-id="e0c7f-118">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c7f-119">CommonParameters</span></span>
<span data-ttu-id="e0c7f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c7f-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0c7f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c7f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0c7f-122">INPUTS</span></span>

## <span data-ttu-id="e0c7f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0c7f-123">OUTPUTS</span></span>

## <span data-ttu-id="e0c7f-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0c7f-124">NOTES</span></span>

## <span data-ttu-id="e0c7f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0c7f-125">RELATED LINKS</span></span>

[<span data-ttu-id="e0c7f-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0c7f-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e0c7f-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0c7f-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e0c7f-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0c7f-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


