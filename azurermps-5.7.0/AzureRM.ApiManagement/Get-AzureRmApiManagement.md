---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 50a548716019f3b5e80cde4b89ae666f5b6199ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610440"
---
# <span data-ttu-id="16b5a-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="16b5a-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="16b5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="16b5a-103">Obtém uma lista ou uma descrição de serviço de gerenciamento de API específica.</span><span class="sxs-lookup"><span data-stu-id="16b5a-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16b5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16b5a-104">SYNTAX</span></span>

### <span data-ttu-id="16b5a-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="16b5a-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16b5a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16b5a-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16b5a-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="16b5a-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16b5a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16b5a-108">DESCRIPTION</span></span>
<span data-ttu-id="16b5a-109">O cmdlet **Get-AzureRmApiManagement** Obtém uma lista de todos os serviços de gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="16b5a-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="16b5a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16b5a-110">EXAMPLES</span></span>

### <span data-ttu-id="16b5a-111">Exemplo 1: obter todos os serviços de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="16b5a-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="16b5a-112">Esse comando obtém todos os serviços de gerenciamento de API em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="16b5a-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="16b5a-113">Exemplo 2: obter todos os serviços de gerenciamento de API por um nome específico</span><span class="sxs-lookup"><span data-stu-id="16b5a-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="16b5a-114">Esse comando obtém todo o serviço de gerenciamento de API por nome.</span><span class="sxs-lookup"><span data-stu-id="16b5a-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="16b5a-115">OS</span><span class="sxs-lookup"><span data-stu-id="16b5a-115">PARAMETERS</span></span>

### <span data-ttu-id="16b5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b5a-116">-DefaultProfile</span></span>
<span data-ttu-id="16b5a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16b5a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="16b5a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="16b5a-118">-Name</span></span>
<span data-ttu-id="16b5a-119">Especifica o nome do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="16b5a-119">Specifies the name of API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16b5a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b5a-120">-ResourceGroupName</span></span>
<span data-ttu-id="16b5a-121">Especifica o nome do grupo de recursos em que esse cmdlet obtém o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="16b5a-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16b5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b5a-122">CommonParameters</span></span>
<span data-ttu-id="16b5a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b5a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16b5a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b5a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16b5a-125">INPUTS</span></span>

### <span data-ttu-id="16b5a-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="16b5a-126">None</span></span>
<span data-ttu-id="16b5a-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="16b5a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16b5a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16b5a-128">OUTPUTS</span></span>

### <span data-ttu-id="16b5a-129">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="16b5a-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="16b5a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16b5a-130">NOTES</span></span>

## <span data-ttu-id="16b5a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16b5a-131">RELATED LINKS</span></span>

[<span data-ttu-id="16b5a-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="16b5a-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="16b5a-133">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="16b5a-133">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="16b5a-134">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="16b5a-134">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="16b5a-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="16b5a-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


