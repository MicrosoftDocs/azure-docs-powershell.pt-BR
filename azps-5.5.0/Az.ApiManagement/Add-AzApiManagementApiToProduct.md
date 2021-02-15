---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118095"
---
# <span data-ttu-id="21e45-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="21e45-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="21e45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21e45-102">SYNOPSIS</span></span>
<span data-ttu-id="21e45-103">Adiciona uma API a um produto.</span><span class="sxs-lookup"><span data-stu-id="21e45-103">Adds an API to a product.</span></span>

## <span data-ttu-id="21e45-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21e45-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21e45-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="21e45-105">DESCRIPTION</span></span>
<span data-ttu-id="21e45-106">O cmdlet **Add-AzApiManagementApiToProduct** adiciona uma API de gerenciamento de API do Azure a um produto.</span><span class="sxs-lookup"><span data-stu-id="21e45-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="21e45-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21e45-107">EXAMPLES</span></span>

### <span data-ttu-id="21e45-108">Exemplo 1: Adicionar uma API a um produto</span><span class="sxs-lookup"><span data-stu-id="21e45-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="21e45-109">Esse comando adiciona a API especificada ao produto especificado.</span><span class="sxs-lookup"><span data-stu-id="21e45-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="21e45-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21e45-110">PARAMETERS</span></span>

### <span data-ttu-id="21e45-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="21e45-111">-ApiId</span></span>
<span data-ttu-id="21e45-112">Especifica a ID de uma API para adicionar a um produto.</span><span class="sxs-lookup"><span data-stu-id="21e45-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e45-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="21e45-113">-Context</span></span>
<span data-ttu-id="21e45-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="21e45-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e45-115">-DefaultProfile</span></span>
<span data-ttu-id="21e45-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="21e45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21e45-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21e45-117">-PassThru</span></span>
<span data-ttu-id="21e45-118">Passthru</span><span class="sxs-lookup"><span data-stu-id="21e45-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e45-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="21e45-119">-ProductId</span></span>
<span data-ttu-id="21e45-120">Especifica a ID do produto ao qual adicionar a API.</span><span class="sxs-lookup"><span data-stu-id="21e45-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e45-121">CommonParameters</span></span>
<span data-ttu-id="21e45-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e45-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21e45-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e45-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="21e45-124">INPUTS</span></span>

### <span data-ttu-id="21e45-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="21e45-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="21e45-126">System.String</span><span class="sxs-lookup"><span data-stu-id="21e45-126">System.String</span></span>

### <span data-ttu-id="21e45-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21e45-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="21e45-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="21e45-128">OUTPUTS</span></span>

### <span data-ttu-id="21e45-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21e45-129">System.Boolean</span></span>

## <span data-ttu-id="21e45-130">Notas</span><span class="sxs-lookup"><span data-stu-id="21e45-130">NOTES</span></span>

## <span data-ttu-id="21e45-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21e45-131">RELATED LINKS</span></span>

[<span data-ttu-id="21e45-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="21e45-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


