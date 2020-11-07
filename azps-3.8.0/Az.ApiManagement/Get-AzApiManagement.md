---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941957"
---
# <span data-ttu-id="0a2d1-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a2d1-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="0a2d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2d1-103">Obtém uma lista ou uma descrição de serviço de gerenciamento de API específica.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="0a2d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a2d1-104">SYNTAX</span></span>

### <span data-ttu-id="0a2d1-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a2d1-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a2d1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a2d1-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a2d1-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="0a2d1-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a2d1-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2d1-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a2d1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a2d1-109">DESCRIPTION</span></span>
<span data-ttu-id="0a2d1-110">O cmdlet **Get-AzApiManagement** Obtém uma lista de todos os serviços de gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="0a2d1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a2d1-111">EXAMPLES</span></span>

### <span data-ttu-id="0a2d1-112">Exemplo 1: obter todos os serviços de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="0a2d1-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="0a2d1-113">Esse comando obtém todos os serviços de gerenciamento de API em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="0a2d1-114">Exemplo 2: obter todos os serviços de gerenciamento de API por um nome específico</span><span class="sxs-lookup"><span data-stu-id="0a2d1-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="0a2d1-115">Esse comando obtém todo o serviço de gerenciamento de API por nome.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="0a2d1-116">OS</span><span class="sxs-lookup"><span data-stu-id="0a2d1-116">PARAMETERS</span></span>

### <span data-ttu-id="0a2d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2d1-117">-DefaultProfile</span></span>
<span data-ttu-id="0a2d1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a2d1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a2d1-119">-Name</span></span>
<span data-ttu-id="0a2d1-120">Especifica o nome do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="0a2d1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2d1-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a2d1-122">Especifica o nome do grupo de recursos em que esse cmdlet obtém o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="0a2d1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2d1-123">-ResourceId</span></span>
<span data-ttu-id="0a2d1-124">Resourcebinding do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="0a2d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2d1-125">CommonParameters</span></span>
<span data-ttu-id="0a2d1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2d1-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a2d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2d1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a2d1-128">INPUTS</span></span>

### <span data-ttu-id="0a2d1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0a2d1-129">System.String</span></span>

## <span data-ttu-id="0a2d1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a2d1-130">OUTPUTS</span></span>

### <span data-ttu-id="0a2d1-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a2d1-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0a2d1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a2d1-132">NOTES</span></span>

## <span data-ttu-id="0a2d1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a2d1-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a2d1-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a2d1-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="0a2d1-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a2d1-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0a2d1-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a2d1-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="0a2d1-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a2d1-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


