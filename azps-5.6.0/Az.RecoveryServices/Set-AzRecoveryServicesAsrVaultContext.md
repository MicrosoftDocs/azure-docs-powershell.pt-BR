---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: ad4fe186a07adb2b9f90222d3caf8def1ecbefdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891299"
---
# <span data-ttu-id="a2206-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="a2206-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="a2206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2206-102">SYNOPSIS</span></span>
<span data-ttu-id="a2206-103">Define o contexto do cofre dos Serviços de Recuperação a ser usado para operações subsequentes de Recuperação de Site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a2206-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a2206-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a2206-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2206-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a2206-105">DESCRIPTION</span></span>
<span data-ttu-id="a2206-106">O cmdlet **Set-AzRecoveryServicesAsrVaultContext** define o contexto do cofre de Recuperação de Site do Azure para operações posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2206-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="a2206-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2206-107">EXAMPLES</span></span>

### <span data-ttu-id="a2206-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2206-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="a2206-109">Define o contexto do cofre como o cofre dos Serviços de Recuperação especificado para operações subsequentes de Recuperação de Site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a2206-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a2206-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a2206-110">PARAMETERS</span></span>

### <span data-ttu-id="a2206-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2206-111">-DefaultProfile</span></span>
<span data-ttu-id="a2206-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a2206-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2206-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="a2206-113">-Vault</span></span>
<span data-ttu-id="a2206-114">O objeto de cofre dos Serviços de Recuperação correspondente ao cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="a2206-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="a2206-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2206-115">-Confirm</span></span>
<span data-ttu-id="a2206-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2206-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2206-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2206-117">-WhatIf</span></span>
<span data-ttu-id="a2206-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2206-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2206-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2206-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2206-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2206-120">CommonParameters</span></span>
<span data-ttu-id="a2206-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2206-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2206-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2206-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2206-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2206-123">INPUTS</span></span>

### <span data-ttu-id="a2206-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a2206-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a2206-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a2206-125">OUTPUTS</span></span>

### <span data-ttu-id="a2206-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a2206-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a2206-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="a2206-127">NOTES</span></span>

## <span data-ttu-id="a2206-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2206-128">RELATED LINKS</span></span>
