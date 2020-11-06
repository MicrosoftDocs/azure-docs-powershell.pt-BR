---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427209"
---
# <span data-ttu-id="a93db-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="a93db-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="a93db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a93db-102">SYNOPSIS</span></span>
<span data-ttu-id="a93db-103">Define o contexto do cofre de serviços de recuperação a ser usado para operações subsequentes do Azure site Recovery na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a93db-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a93db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a93db-104">SYNTAX</span></span>

### <span data-ttu-id="a93db-105">AzureRecoveryServicesVault (padrão)</span><span class="sxs-lookup"><span data-stu-id="a93db-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a93db-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a93db-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a93db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a93db-107">DESCRIPTION</span></span>
<span data-ttu-id="a93db-108">O cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** define o contexto do cofre do Azure site Recovery para outras operações.</span><span class="sxs-lookup"><span data-stu-id="a93db-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="a93db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a93db-109">EXAMPLES</span></span>

### <span data-ttu-id="a93db-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a93db-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="a93db-111">Define o contexto do cofre para o cofre de serviços de recuperação especificado para operações subsequentes de recuperação de site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a93db-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a93db-112">OS</span><span class="sxs-lookup"><span data-stu-id="a93db-112">PARAMETERS</span></span>

### <span data-ttu-id="a93db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93db-113">-DefaultProfile</span></span>
<span data-ttu-id="a93db-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a93db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93db-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a93db-115">-ResourceId</span></span>
<span data-ttu-id="a93db-116">Especifica o ID do recurso de cofre recoveryservices ser definido como contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="a93db-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93db-117">-Cofre</span><span class="sxs-lookup"><span data-stu-id="a93db-117">-Vault</span></span>
<span data-ttu-id="a93db-118">O objeto do cofre de serviços de recuperação correspondente ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a93db-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93db-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a93db-119">-Confirm</span></span>
<span data-ttu-id="a93db-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93db-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a93db-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93db-121">-WhatIf</span></span>
<span data-ttu-id="a93db-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a93db-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a93db-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a93db-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a93db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93db-124">CommonParameters</span></span>
<span data-ttu-id="a93db-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93db-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93db-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a93db-127">INPUTS</span></span>

### <span data-ttu-id="a93db-128">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a93db-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a93db-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a93db-129">OUTPUTS</span></span>

### <span data-ttu-id="a93db-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a93db-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a93db-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a93db-131">NOTES</span></span>

## <span data-ttu-id="a93db-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a93db-132">RELATED LINKS</span></span>