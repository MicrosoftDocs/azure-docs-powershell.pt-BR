---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: a4a6cf459c253c26f5d550492f8b756d59fcdf44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890896"
---
# <span data-ttu-id="c0c06-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0c06-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="c0c06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c06-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c06-103">Obtém uma lista ou uma descrição específica do Serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c0c06-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="c0c06-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0c06-104">SYNTAX</span></span>

### <span data-ttu-id="c0c06-105">GetBySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c0c06-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0c06-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0c06-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0c06-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="c0c06-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0c06-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0c06-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0c06-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0c06-109">DESCRIPTION</span></span>
<span data-ttu-id="c0c06-110">O cmdlet **Get-AzApiManagement** obtém uma lista de todos os serviços de Gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="c0c06-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="c0c06-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0c06-111">EXAMPLES</span></span>

### <span data-ttu-id="c0c06-112">Exemplo 1: Obter todos os serviços de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="c0c06-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="c0c06-113">Esse comando obtém todos os serviços de Gerenciamento de API dentro de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c0c06-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="c0c06-114">Exemplo 2: Obter todos os serviços de Gerenciamento de API por um nome específico</span><span class="sxs-lookup"><span data-stu-id="c0c06-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="c0c06-115">Este comando obtém todos os serviços de Gerenciamento de API pelo nome.</span><span class="sxs-lookup"><span data-stu-id="c0c06-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="c0c06-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0c06-116">PARAMETERS</span></span>

### <span data-ttu-id="c0c06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c06-117">-DefaultProfile</span></span>
<span data-ttu-id="c0c06-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c0c06-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c06-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c06-119">-Name</span></span>
<span data-ttu-id="c0c06-120">Especifica o nome do serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c0c06-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="c0c06-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c06-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0c06-122">Especifica o nome do grupo de recursos no qual este cmdlet obtém o serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c0c06-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="c0c06-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0c06-123">-ResourceId</span></span>
<span data-ttu-id="c0c06-124">Arm ResourceId do serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c0c06-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="c0c06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c06-125">CommonParameters</span></span>
<span data-ttu-id="c0c06-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c06-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0c06-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c06-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0c06-128">INPUTS</span></span>

### <span data-ttu-id="c0c06-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c0c06-129">System.String</span></span>

## <span data-ttu-id="c0c06-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0c06-130">OUTPUTS</span></span>

### <span data-ttu-id="c0c06-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0c06-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c0c06-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0c06-132">NOTES</span></span>

## <span data-ttu-id="c0c06-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0c06-133">RELATED LINKS</span></span>

[<span data-ttu-id="c0c06-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0c06-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="c0c06-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0c06-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="c0c06-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0c06-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="c0c06-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c0c06-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


