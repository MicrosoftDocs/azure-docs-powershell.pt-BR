---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426838"
---
# <span data-ttu-id="d6dec-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d6dec-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="d6dec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6dec-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dec-103">Remove uma propriedade de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d6dec-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6dec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6dec-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6dec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6dec-105">DESCRIPTION</span></span>
<span data-ttu-id="d6dec-106">O cmdlet **Remove-AzureRmApiManagementProperty** remove uma **Propriedade** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dec-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="d6dec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6dec-107">EXAMPLES</span></span>

### <span data-ttu-id="d6dec-108">Exemplo 1: remover uma propriedade</span><span class="sxs-lookup"><span data-stu-id="d6dec-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="d6dec-109">Esse comando Remove a propriedade que tem a ID Property11.</span><span class="sxs-lookup"><span data-stu-id="d6dec-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="d6dec-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6dec-110">PARAMETERS</span></span>

### <span data-ttu-id="d6dec-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d6dec-111">-Context</span></span>
<span data-ttu-id="d6dec-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d6dec-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6dec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dec-113">-DefaultProfile</span></span>
<span data-ttu-id="d6dec-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d6dec-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6dec-115">-PassThru</span></span>
<span data-ttu-id="d6dec-116">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d6dec-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="d6dec-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="d6dec-117">-PropertyId</span></span>
<span data-ttu-id="d6dec-118">Especifica uma ID da propriedade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d6dec-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6dec-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6dec-119">-Confirm</span></span>
<span data-ttu-id="d6dec-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6dec-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6dec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6dec-121">-WhatIf</span></span>
<span data-ttu-id="d6dec-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6dec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6dec-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6dec-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6dec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dec-124">CommonParameters</span></span>
<span data-ttu-id="d6dec-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dec-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dec-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6dec-127">INPUTS</span></span>

### <span data-ttu-id="d6dec-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d6dec-128">None</span></span>
<span data-ttu-id="d6dec-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d6dec-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6dec-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6dec-130">OUTPUTS</span></span>

### <span data-ttu-id="d6dec-131">bool</span><span class="sxs-lookup"><span data-stu-id="d6dec-131">bool</span></span>

## <span data-ttu-id="d6dec-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6dec-132">NOTES</span></span>

## <span data-ttu-id="d6dec-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6dec-133">RELATED LINKS</span></span>

[<span data-ttu-id="d6dec-134">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d6dec-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="d6dec-135">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d6dec-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


