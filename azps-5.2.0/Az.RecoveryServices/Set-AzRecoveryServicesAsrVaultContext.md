---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257159"
---
# <span data-ttu-id="e00fc-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="e00fc-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="e00fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e00fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e00fc-103">Define o contexto do cofre de serviços de recuperação a ser usado para operações subsequentes do Azure site Recovery na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e00fc-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="e00fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e00fc-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e00fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e00fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e00fc-106">O cmdlet **set-AzRecoveryServicesAsrVaultContext** define o contexto do cofre do Azure site Recovery para outras operações.</span><span class="sxs-lookup"><span data-stu-id="e00fc-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="e00fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e00fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e00fc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e00fc-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="e00fc-109">Define o contexto do cofre para o cofre de serviços de recuperação especificado para operações subsequentes de recuperação de site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e00fc-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="e00fc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e00fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e00fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00fc-111">-DefaultProfile</span></span>
<span data-ttu-id="e00fc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e00fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00fc-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="e00fc-113">-Vault</span></span>
<span data-ttu-id="e00fc-114">O objeto do cofre de serviços de recuperação correspondente ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e00fc-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e00fc-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e00fc-115">-Confirm</span></span>
<span data-ttu-id="e00fc-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e00fc-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00fc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e00fc-117">-WhatIf</span></span>
<span data-ttu-id="e00fc-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e00fc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e00fc-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e00fc-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00fc-120">CommonParameters</span></span>
<span data-ttu-id="e00fc-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e00fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00fc-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e00fc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00fc-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e00fc-123">INPUTS</span></span>

### <span data-ttu-id="e00fc-124">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e00fc-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e00fc-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e00fc-125">OUTPUTS</span></span>

### <span data-ttu-id="e00fc-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="e00fc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="e00fc-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e00fc-127">NOTES</span></span>

## <span data-ttu-id="e00fc-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e00fc-128">RELATED LINKS</span></span>
