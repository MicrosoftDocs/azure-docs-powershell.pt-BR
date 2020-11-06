---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426841"
---
# <span data-ttu-id="c1cef-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="c1cef-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="c1cef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1cef-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cef-103">Remove um produto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="c1cef-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1cef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1cef-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1cef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1cef-105">DESCRIPTION</span></span>
<span data-ttu-id="c1cef-106">O cmdlet **Remove-AzureRmApiManagementProductFromGroup** remove um produto de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c1cef-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="c1cef-107">Em outras palavras, esse cmdlet Remove a atribuição de grupo de um produto.</span><span class="sxs-lookup"><span data-stu-id="c1cef-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="c1cef-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1cef-108">EXAMPLES</span></span>

### <span data-ttu-id="c1cef-109">Exemplo 1: remover um produto de um grupo</span><span class="sxs-lookup"><span data-stu-id="c1cef-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c1cef-110">Esse comando Remove um produto de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c1cef-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="c1cef-111">OS</span><span class="sxs-lookup"><span data-stu-id="c1cef-111">PARAMETERS</span></span>

### <span data-ttu-id="c1cef-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c1cef-112">-Context</span></span>
<span data-ttu-id="c1cef-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c1cef-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c1cef-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c1cef-114">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cef-115">-DefaultProfile</span></span>
<span data-ttu-id="c1cef-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c1cef-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c1cef-117">-GroupId</span></span>
<span data-ttu-id="c1cef-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="c1cef-118">Specifies the group ID.</span></span>
<span data-ttu-id="c1cef-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c1cef-119">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cef-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1cef-120">-PassThru</span></span>
<span data-ttu-id="c1cef-121">Indica que esse cmdlet retorna um valor de $True, se tiver êxito ou $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c1cef-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cef-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c1cef-122">-ProductId</span></span>
<span data-ttu-id="c1cef-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="c1cef-123">Specifies the product ID.</span></span>
<span data-ttu-id="c1cef-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c1cef-124">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cef-125">CommonParameters</span></span>
<span data-ttu-id="c1cef-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1cef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cef-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1cef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cef-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1cef-128">INPUTS</span></span>

### <span data-ttu-id="c1cef-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c1cef-129">None</span></span>
<span data-ttu-id="c1cef-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c1cef-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1cef-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1cef-131">OUTPUTS</span></span>

### <span data-ttu-id="c1cef-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1cef-132">System.Boolean</span></span>

## <span data-ttu-id="c1cef-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1cef-133">NOTES</span></span>

## <span data-ttu-id="c1cef-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1cef-134">RELATED LINKS</span></span>

[<span data-ttu-id="c1cef-135">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c1cef-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


