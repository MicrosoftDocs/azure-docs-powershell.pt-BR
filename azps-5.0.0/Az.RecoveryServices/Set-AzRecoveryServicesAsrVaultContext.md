---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115703"
---
# <span data-ttu-id="1c537-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="1c537-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="1c537-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c537-102">SYNOPSIS</span></span>
<span data-ttu-id="1c537-103">Define o contexto do cofre de serviços de recuperação a ser usado para operações subsequentes do Azure site Recovery na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1c537-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="1c537-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c537-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c537-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c537-105">DESCRIPTION</span></span>
<span data-ttu-id="1c537-106">O cmdlet **set-AzRecoveryServicesAsrVaultContext** define o contexto do cofre do Azure site Recovery para outras operações.</span><span class="sxs-lookup"><span data-stu-id="1c537-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="1c537-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c537-107">EXAMPLES</span></span>

### <span data-ttu-id="1c537-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c537-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="1c537-109">Define o contexto do cofre para o cofre de serviços de recuperação especificado para operações subsequentes de recuperação de site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1c537-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="1c537-110">OS</span><span class="sxs-lookup"><span data-stu-id="1c537-110">PARAMETERS</span></span>

### <span data-ttu-id="1c537-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c537-111">-DefaultProfile</span></span>
<span data-ttu-id="1c537-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c537-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c537-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="1c537-113">-Vault</span></span>
<span data-ttu-id="1c537-114">O objeto do cofre de serviços de recuperação correspondente ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1c537-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="1c537-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c537-115">-Confirm</span></span>
<span data-ttu-id="1c537-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c537-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c537-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c537-117">-WhatIf</span></span>
<span data-ttu-id="1c537-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c537-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c537-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c537-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c537-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c537-120">CommonParameters</span></span>
<span data-ttu-id="1c537-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c537-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c537-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c537-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c537-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c537-123">INPUTS</span></span>

### <span data-ttu-id="1c537-124">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="1c537-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1c537-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c537-125">OUTPUTS</span></span>

### <span data-ttu-id="1c537-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1c537-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="1c537-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c537-127">NOTES</span></span>

## <span data-ttu-id="1c537-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c537-128">RELATED LINKS</span></span>
