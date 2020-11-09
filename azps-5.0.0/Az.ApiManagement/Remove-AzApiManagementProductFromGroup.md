---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284135"
---
# <span data-ttu-id="1c38a-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="1c38a-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="1c38a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c38a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c38a-103">Remove um produto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="1c38a-103">Removes a product from a group.</span></span>

## <span data-ttu-id="1c38a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c38a-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c38a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c38a-105">DESCRIPTION</span></span>
<span data-ttu-id="1c38a-106">O cmdlet **Remove-AzApiManagementProductFromGroup** remove um produto de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="1c38a-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="1c38a-107">Em outras palavras, esse cmdlet Remove a atribuição de grupo de um produto.</span><span class="sxs-lookup"><span data-stu-id="1c38a-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="1c38a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c38a-108">EXAMPLES</span></span>

### <span data-ttu-id="1c38a-109">Exemplo 1: remover um produto de um grupo</span><span class="sxs-lookup"><span data-stu-id="1c38a-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="1c38a-110">Esse comando Remove um produto de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="1c38a-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="1c38a-111">OS</span><span class="sxs-lookup"><span data-stu-id="1c38a-111">PARAMETERS</span></span>

### <span data-ttu-id="1c38a-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1c38a-112">-Context</span></span>
<span data-ttu-id="1c38a-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1c38a-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1c38a-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1c38a-114">This parameter is required.</span></span>

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

### <span data-ttu-id="1c38a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c38a-115">-DefaultProfile</span></span>
<span data-ttu-id="1c38a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c38a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c38a-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1c38a-117">-GroupId</span></span>
<span data-ttu-id="1c38a-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="1c38a-118">Specifies the group ID.</span></span>
<span data-ttu-id="1c38a-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1c38a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="1c38a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c38a-120">-PassThru</span></span>
<span data-ttu-id="1c38a-121">Indica que esse cmdlet retorna um valor de $True, se tiver êxito ou $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1c38a-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="1c38a-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1c38a-122">-ProductId</span></span>
<span data-ttu-id="1c38a-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="1c38a-123">Specifies the product ID.</span></span>
<span data-ttu-id="1c38a-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1c38a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="1c38a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c38a-125">CommonParameters</span></span>
<span data-ttu-id="1c38a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c38a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c38a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c38a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c38a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c38a-128">INPUTS</span></span>

### <span data-ttu-id="1c38a-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1c38a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c38a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1c38a-130">System.String</span></span>

### <span data-ttu-id="1c38a-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c38a-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c38a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c38a-132">OUTPUTS</span></span>

### <span data-ttu-id="1c38a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c38a-133">System.Boolean</span></span>

## <span data-ttu-id="1c38a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c38a-134">NOTES</span></span>

## <span data-ttu-id="1c38a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c38a-135">RELATED LINKS</span></span>

[<span data-ttu-id="1c38a-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="1c38a-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


