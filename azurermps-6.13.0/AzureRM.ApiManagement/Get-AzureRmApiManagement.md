---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: bff36b7bcb37dd099f9aa50a99bed9538111e8d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433343"
---
# <span data-ttu-id="56500-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="56500-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="56500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56500-102">SYNOPSIS</span></span>
<span data-ttu-id="56500-103">Obtém uma lista ou uma descrição de serviço de gerenciamento de API específica.</span><span class="sxs-lookup"><span data-stu-id="56500-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56500-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56500-104">SYNTAX</span></span>

### <span data-ttu-id="56500-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="56500-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56500-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56500-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56500-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="56500-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56500-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56500-108">DESCRIPTION</span></span>
<span data-ttu-id="56500-109">O cmdlet **Get-AzureRmApiManagement** Obtém uma lista de todos os serviços de gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="56500-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="56500-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56500-110">EXAMPLES</span></span>

### <span data-ttu-id="56500-111">Exemplo 1: obter todos os serviços de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="56500-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="56500-112">Esse comando obtém todos os serviços de gerenciamento de API em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="56500-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="56500-113">Exemplo 2: obter todos os serviços de gerenciamento de API por um nome específico</span><span class="sxs-lookup"><span data-stu-id="56500-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="56500-114">Esse comando obtém todo o serviço de gerenciamento de API por nome.</span><span class="sxs-lookup"><span data-stu-id="56500-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="56500-115">OS</span><span class="sxs-lookup"><span data-stu-id="56500-115">PARAMETERS</span></span>

### <span data-ttu-id="56500-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56500-116">-DefaultProfile</span></span>
<span data-ttu-id="56500-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56500-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56500-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="56500-118">-Name</span></span>
<span data-ttu-id="56500-119">Especifica o nome do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="56500-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56500-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56500-120">-ResourceGroupName</span></span>
<span data-ttu-id="56500-121">Especifica o nome do grupo de recursos em que esse cmdlet obtém o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="56500-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56500-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56500-122">CommonParameters</span></span>
<span data-ttu-id="56500-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56500-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56500-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56500-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56500-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56500-125">INPUTS</span></span>

### <span data-ttu-id="56500-126">System. String</span><span class="sxs-lookup"><span data-stu-id="56500-126">System.String</span></span>

## <span data-ttu-id="56500-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56500-127">OUTPUTS</span></span>

### <span data-ttu-id="56500-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="56500-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="56500-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56500-129">NOTES</span></span>

## <span data-ttu-id="56500-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56500-130">RELATED LINKS</span></span>

[<span data-ttu-id="56500-131">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="56500-131">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="56500-132">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="56500-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="56500-133">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="56500-133">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="56500-134">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="56500-134">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


