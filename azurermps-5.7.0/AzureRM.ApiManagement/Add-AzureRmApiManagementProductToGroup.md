---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: f7c1db6b4ce7c9df63506cdba8b1a206c22ee03e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610950"
---
# <span data-ttu-id="95e35-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="95e35-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="95e35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95e35-102">SYNOPSIS</span></span>
<span data-ttu-id="95e35-103">Adiciona um produto a um grupo.</span><span class="sxs-lookup"><span data-stu-id="95e35-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95e35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95e35-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95e35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95e35-105">DESCRIPTION</span></span>
<span data-ttu-id="95e35-106">O cmdlet **Add-AzureRmApiManagementProductToGroup** adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="95e35-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="95e35-107">Em outras palavras, esse cmdlet atribui um grupo a um produto.</span><span class="sxs-lookup"><span data-stu-id="95e35-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="95e35-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95e35-108">EXAMPLES</span></span>

### <span data-ttu-id="95e35-109">Exemplo 1: adicionar um produto a um grupo</span><span class="sxs-lookup"><span data-stu-id="95e35-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="95e35-110">Esse comando adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="95e35-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="95e35-111">OS</span><span class="sxs-lookup"><span data-stu-id="95e35-111">PARAMETERS</span></span>

### <span data-ttu-id="95e35-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="95e35-112">-Context</span></span>
<span data-ttu-id="95e35-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="95e35-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="95e35-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="95e35-114">This parameter is required.</span></span>

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

### <span data-ttu-id="95e35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e35-115">-DefaultProfile</span></span>
<span data-ttu-id="95e35-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95e35-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="95e35-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="95e35-117">-GroupId</span></span>
<span data-ttu-id="95e35-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="95e35-118">Specifies the group ID.</span></span>
<span data-ttu-id="95e35-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="95e35-119">This parameter is required.</span></span>

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

### <span data-ttu-id="95e35-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95e35-120">-PassThru</span></span>
<span data-ttu-id="95e35-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="95e35-121">passthru</span></span>

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

### <span data-ttu-id="95e35-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="95e35-122">-ProductId</span></span>
<span data-ttu-id="95e35-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="95e35-123">Specifies the product ID.</span></span>
<span data-ttu-id="95e35-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="95e35-124">This parameter is required.</span></span>

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

### <span data-ttu-id="95e35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e35-125">CommonParameters</span></span>
<span data-ttu-id="95e35-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e35-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95e35-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e35-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95e35-128">INPUTS</span></span>

### <span data-ttu-id="95e35-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="95e35-129">None</span></span>
<span data-ttu-id="95e35-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="95e35-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95e35-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95e35-131">OUTPUTS</span></span>

### <span data-ttu-id="95e35-132">Booliana</span><span class="sxs-lookup"><span data-stu-id="95e35-132">Boolean</span></span>

## <span data-ttu-id="95e35-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95e35-133">NOTES</span></span>

## <span data-ttu-id="95e35-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95e35-134">RELATED LINKS</span></span>

[<span data-ttu-id="95e35-135">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="95e35-135">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


