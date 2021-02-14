---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111241"
---
# <span data-ttu-id="9dbd7-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="9dbd7-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="9dbd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbd7-103">Remove uma API de um produto.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-103">Removes an API from a product.</span></span>

## <span data-ttu-id="9dbd7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dbd7-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dbd7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9dbd7-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbd7-106">O cmdlet **Remove-AzApiManagementApiFromProduct** remove uma API de gerenciamento de API do Azure de um produto.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="9dbd7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9dbd7-107">EXAMPLES</span></span>

### <span data-ttu-id="9dbd7-108">Exemplo 1: Remover uma API de um produto</span><span class="sxs-lookup"><span data-stu-id="9dbd7-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="9dbd7-109">Esse comando remove a API especificada de um produto.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="9dbd7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dbd7-110">PARAMETERS</span></span>

### <span data-ttu-id="9dbd7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9dbd7-111">-ApiId</span></span>
<span data-ttu-id="9dbd7-112">Especifica a ID da API a ser removido do produto.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="9dbd7-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9dbd7-113">-Context</span></span>
<span data-ttu-id="9dbd7-114">Especifica um **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9dbd7-114">Specifies a **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dbd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbd7-115">-DefaultProfile</span></span>
<span data-ttu-id="9dbd7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dbd7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dbd7-117">-PassThru</span></span>
<span data-ttu-id="9dbd7-118">Indica que esse cmdlet retorna um valor de $True se for bem-sucedido ou $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="9dbd7-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9dbd7-119">-ProductId</span></span>
<span data-ttu-id="9dbd7-120">Especifica a ID do produto do qual a API será removido.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="9dbd7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbd7-121">CommonParameters</span></span>
<span data-ttu-id="9dbd7-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbd7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbd7-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dbd7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbd7-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="9dbd7-124">INPUTS</span></span>

### <span data-ttu-id="9dbd7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9dbd7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9dbd7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9dbd7-126">System.String</span></span>

### <span data-ttu-id="9dbd7-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9dbd7-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9dbd7-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="9dbd7-128">OUTPUTS</span></span>

### <span data-ttu-id="9dbd7-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9dbd7-129">System.Boolean</span></span>

## <span data-ttu-id="9dbd7-130">Notas</span><span class="sxs-lookup"><span data-stu-id="9dbd7-130">NOTES</span></span>

## <span data-ttu-id="9dbd7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dbd7-131">RELATED LINKS</span></span>

[<span data-ttu-id="9dbd7-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="9dbd7-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


