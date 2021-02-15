---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118094"
---
# <span data-ttu-id="33ef5-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="33ef5-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="33ef5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="33ef5-103">Adiciona um produto a um grupo.</span><span class="sxs-lookup"><span data-stu-id="33ef5-103">Adds a product to a group.</span></span>

## <span data-ttu-id="33ef5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33ef5-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ef5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="33ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="33ef5-106">O **cmdlet Add-AzApiManagementProductToGroup** adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="33ef5-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="33ef5-107">Em outras palavras, este cmdlet atribui um grupo a um produto.</span><span class="sxs-lookup"><span data-stu-id="33ef5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="33ef5-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33ef5-108">EXAMPLES</span></span>

### <span data-ttu-id="33ef5-109">Exemplo 1: Adicionar um produto a um grupo</span><span class="sxs-lookup"><span data-stu-id="33ef5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="33ef5-110">Esse comando adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="33ef5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="33ef5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33ef5-111">PARAMETERS</span></span>

### <span data-ttu-id="33ef5-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="33ef5-112">-Context</span></span>
<span data-ttu-id="33ef5-113">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="33ef5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="33ef5-114">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="33ef5-114">This parameter is required.</span></span>

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

### <span data-ttu-id="33ef5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ef5-115">-DefaultProfile</span></span>
<span data-ttu-id="33ef5-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="33ef5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33ef5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="33ef5-117">-GroupId</span></span>
<span data-ttu-id="33ef5-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="33ef5-118">Specifies the group ID.</span></span>
<span data-ttu-id="33ef5-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="33ef5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="33ef5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33ef5-120">-PassThru</span></span>
<span data-ttu-id="33ef5-121">Passthru</span><span class="sxs-lookup"><span data-stu-id="33ef5-121">passthru</span></span>

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

### <span data-ttu-id="33ef5-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="33ef5-122">-ProductId</span></span>
<span data-ttu-id="33ef5-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="33ef5-123">Specifies the product ID.</span></span>
<span data-ttu-id="33ef5-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="33ef5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="33ef5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ef5-125">CommonParameters</span></span>
<span data-ttu-id="33ef5-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ef5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ef5-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33ef5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ef5-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="33ef5-128">INPUTS</span></span>

### <span data-ttu-id="33ef5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33ef5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33ef5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="33ef5-130">System.String</span></span>

### <span data-ttu-id="33ef5-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33ef5-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33ef5-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="33ef5-132">OUTPUTS</span></span>

### <span data-ttu-id="33ef5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33ef5-133">System.Boolean</span></span>

## <span data-ttu-id="33ef5-134">Notas</span><span class="sxs-lookup"><span data-stu-id="33ef5-134">NOTES</span></span>

## <span data-ttu-id="33ef5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33ef5-135">RELATED LINKS</span></span>

[<span data-ttu-id="33ef5-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="33ef5-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


