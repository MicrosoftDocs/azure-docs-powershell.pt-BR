---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 3345b48b7956e9a2e8c82d28dd87ec254bf85544
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595710"
---
# <span data-ttu-id="098a9-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="098a9-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="098a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="098a9-102">SYNOPSIS</span></span>
<span data-ttu-id="098a9-103">Adiciona um produto a um grupo.</span><span class="sxs-lookup"><span data-stu-id="098a9-103">Adds a product to a group.</span></span>

## <span data-ttu-id="098a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="098a9-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="098a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="098a9-105">DESCRIPTION</span></span>
<span data-ttu-id="098a9-106">O cmdlet **Add-AzApiManagementProductToGroup** adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="098a9-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="098a9-107">Em outras palavras, esse cmdlet atribui um grupo a um produto.</span><span class="sxs-lookup"><span data-stu-id="098a9-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="098a9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="098a9-108">EXAMPLES</span></span>

### <span data-ttu-id="098a9-109">Exemplo 1: adicionar um produto a um grupo</span><span class="sxs-lookup"><span data-stu-id="098a9-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="098a9-110">Esse comando adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="098a9-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="098a9-111">OS</span><span class="sxs-lookup"><span data-stu-id="098a9-111">PARAMETERS</span></span>

### <span data-ttu-id="098a9-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="098a9-112">-Context</span></span>
<span data-ttu-id="098a9-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="098a9-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="098a9-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="098a9-114">This parameter is required.</span></span>

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

### <span data-ttu-id="098a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098a9-115">-DefaultProfile</span></span>
<span data-ttu-id="098a9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="098a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098a9-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="098a9-117">-GroupId</span></span>
<span data-ttu-id="098a9-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="098a9-118">Specifies the group ID.</span></span>
<span data-ttu-id="098a9-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="098a9-119">This parameter is required.</span></span>

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

### <span data-ttu-id="098a9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="098a9-120">-PassThru</span></span>
<span data-ttu-id="098a9-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="098a9-121">passthru</span></span>

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

### <span data-ttu-id="098a9-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="098a9-122">-ProductId</span></span>
<span data-ttu-id="098a9-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="098a9-123">Specifies the product ID.</span></span>
<span data-ttu-id="098a9-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="098a9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="098a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098a9-125">CommonParameters</span></span>
<span data-ttu-id="098a9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098a9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="098a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098a9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="098a9-128">INPUTS</span></span>

### <span data-ttu-id="098a9-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="098a9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="098a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="098a9-130">System.String</span></span>

### <span data-ttu-id="098a9-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="098a9-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="098a9-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="098a9-132">OUTPUTS</span></span>

### <span data-ttu-id="098a9-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="098a9-133">System.Boolean</span></span>

## <span data-ttu-id="098a9-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="098a9-134">NOTES</span></span>

## <span data-ttu-id="098a9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="098a9-135">RELATED LINKS</span></span>

[<span data-ttu-id="098a9-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="098a9-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


