---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429719"
---
# <span data-ttu-id="6a0c9-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="6a0c9-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="6a0c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a0c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0c9-103">Define o contexto do cofre de serviços de recuperação a ser usado para operações subsequentes do Azure site Recovery na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a0c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a0c9-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a0c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a0c9-105">DESCRIPTION</span></span>
<span data-ttu-id="6a0c9-106">O cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** define o contexto do cofre do Azure site Recovery para outras operações.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="6a0c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a0c9-107">EXAMPLES</span></span>

### <span data-ttu-id="6a0c9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a0c9-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="6a0c9-109">Define o contexto do cofre para o cofre de serviços de recuperação especificado para operações subsequentes de recuperação de site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="6a0c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="6a0c9-110">PARAMETERS</span></span>

### <span data-ttu-id="6a0c9-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a0c9-111">-Confirm</span></span>
<span data-ttu-id="6a0c9-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a0c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0c9-113">-DefaultProfile</span></span>
<span data-ttu-id="6a0c9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c9-115">-Cofre</span><span class="sxs-lookup"><span data-stu-id="6a0c9-115">-Vault</span></span>
<span data-ttu-id="6a0c9-116">O objeto do cofre de serviços de recuperação correspondente ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="6a0c9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0c9-117">-WhatIf</span></span>
<span data-ttu-id="6a0c9-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a0c9-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a0c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0c9-120">CommonParameters</span></span>
<span data-ttu-id="6a0c9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0c9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0c9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0c9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a0c9-123">INPUTS</span></span>

### <span data-ttu-id="6a0c9-124">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="6a0c9-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6a0c9-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a0c9-125">OUTPUTS</span></span>

### <span data-ttu-id="6a0c9-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="6a0c9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="6a0c9-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a0c9-127">NOTES</span></span>

## <span data-ttu-id="6a0c9-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a0c9-128">RELATED LINKS</span></span>
