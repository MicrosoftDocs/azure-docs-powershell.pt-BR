---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429151"
---
# <span data-ttu-id="b9f81-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b9f81-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b9f81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9f81-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f81-103">Define o contexto do cofre de serviços de recuperação a ser usado para operações subsequentes do Azure site Recovery na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9f81-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9f81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9f81-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9f81-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9f81-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f81-106">O cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** define o contexto do cofre do Azure site Recovery para outras operações.</span><span class="sxs-lookup"><span data-stu-id="b9f81-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="b9f81-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9f81-107">EXAMPLES</span></span>

### <span data-ttu-id="b9f81-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9f81-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="b9f81-109">Define o contexto do cofre para o cofre de serviços de recuperação especificado para operações subsequentes de recuperação de site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9f81-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="b9f81-110">OS</span><span class="sxs-lookup"><span data-stu-id="b9f81-110">PARAMETERS</span></span>

### <span data-ttu-id="b9f81-111">-Cofre</span><span class="sxs-lookup"><span data-stu-id="b9f81-111">-Vault</span></span>
<span data-ttu-id="b9f81-112">O objeto do cofre de serviços de recuperação correspondente ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b9f81-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9f81-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9f81-113">-Confirm</span></span>
<span data-ttu-id="b9f81-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9f81-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f81-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f81-115">-WhatIf</span></span>
<span data-ttu-id="b9f81-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9f81-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9f81-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9f81-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f81-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f81-118">CommonParameters</span></span>
<span data-ttu-id="b9f81-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f81-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f81-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f81-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f81-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9f81-121">INPUTS</span></span>

### <span data-ttu-id="b9f81-122">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b9f81-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b9f81-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9f81-123">OUTPUTS</span></span>

### <span data-ttu-id="b9f81-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b9f81-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b9f81-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9f81-125">NOTES</span></span>

## <span data-ttu-id="b9f81-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9f81-126">RELATED LINKS</span></span>

