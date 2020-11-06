---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428831"
---
# <span data-ttu-id="d70db-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d70db-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d70db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d70db-102">SYNOPSIS</span></span>
<span data-ttu-id="d70db-103">Obtém um plano de recuperação ou todos os planos de recuperação no cofre dos serviços de recuperação</span><span class="sxs-lookup"><span data-stu-id="d70db-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d70db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d70db-104">SYNTAX</span></span>

### <span data-ttu-id="d70db-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="d70db-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70db-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d70db-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70db-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d70db-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d70db-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d70db-108">DESCRIPTION</span></span>
<span data-ttu-id="d70db-109">O cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPlan** Obtém os detalhes do plano de recuperação especificado ou todos os planos de recuperação no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d70db-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="d70db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d70db-110">EXAMPLES</span></span>

### <span data-ttu-id="d70db-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d70db-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="d70db-112">Obtém o plano de recuperação com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="d70db-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="d70db-113">OS</span><span class="sxs-lookup"><span data-stu-id="d70db-113">PARAMETERS</span></span>

### <span data-ttu-id="d70db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70db-114">-DefaultProfile</span></span>
<span data-ttu-id="d70db-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d70db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="d70db-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d70db-116">-FriendlyName</span></span>
<span data-ttu-id="d70db-117">Especifica o nome amigável do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="d70db-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70db-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d70db-118">-Name</span></span>
<span data-ttu-id="d70db-119">Especifica o nome do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="d70db-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70db-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d70db-120">-Path</span></span>
<span data-ttu-id="d70db-121">Especifica o caminho de arquivo para o qual esse cmdlet salva a definição JSON do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d70db-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="d70db-122">A definição JSON pode ser editada para modificar o plano de recuperação e usada para atualizar o plano de recuperação por meio do cmdlet Update-AzureRmRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d70db-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70db-123">CommonParameters</span></span>
<span data-ttu-id="d70db-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d70db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70db-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d70db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70db-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d70db-126">INPUTS</span></span>

### <span data-ttu-id="d70db-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d70db-127">None</span></span>

## <span data-ttu-id="d70db-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d70db-128">OUTPUTS</span></span>

### <span data-ttu-id="d70db-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d70db-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d70db-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d70db-130">NOTES</span></span>

## <span data-ttu-id="d70db-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d70db-131">RELATED LINKS</span></span>

[<span data-ttu-id="d70db-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d70db-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d70db-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d70db-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d70db-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d70db-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)