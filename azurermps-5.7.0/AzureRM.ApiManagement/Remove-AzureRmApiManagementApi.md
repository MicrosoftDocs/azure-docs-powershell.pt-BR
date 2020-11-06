---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610682"
---
# <span data-ttu-id="447f4-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="447f4-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="447f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="447f4-102">SYNOPSIS</span></span>
<span data-ttu-id="447f4-103">Remove uma API.</span><span class="sxs-lookup"><span data-stu-id="447f4-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="447f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="447f4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="447f4-105">DESCRIPTION</span></span>
<span data-ttu-id="447f4-106">O cmdlet **Remove-AzureRmApiManagementApi** remove uma API existente.</span><span class="sxs-lookup"><span data-stu-id="447f4-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="447f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="447f4-107">EXAMPLES</span></span>

### <span data-ttu-id="447f4-108">Exemplo 1: remover uma API</span><span class="sxs-lookup"><span data-stu-id="447f4-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="447f4-109">Este comando Remove a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="447f4-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="447f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="447f4-110">PARAMETERS</span></span>

### <span data-ttu-id="447f4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="447f4-111">-ApiId</span></span>
<span data-ttu-id="447f4-112">Especifica a ID da API remove.</span><span class="sxs-lookup"><span data-stu-id="447f4-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="447f4-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="447f4-113">-Context</span></span>
<span data-ttu-id="447f4-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="447f4-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="447f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447f4-115">-DefaultProfile</span></span>
<span data-ttu-id="447f4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="447f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="447f4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="447f4-117">-PassThru</span></span>
<span data-ttu-id="447f4-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="447f4-118">passthru</span></span>

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

### <span data-ttu-id="447f4-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="447f4-119">-Confirm</span></span>
<span data-ttu-id="447f4-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="447f4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="447f4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="447f4-121">-WhatIf</span></span>
<span data-ttu-id="447f4-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="447f4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="447f4-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="447f4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="447f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447f4-124">CommonParameters</span></span>
<span data-ttu-id="447f4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447f4-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447f4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447f4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="447f4-127">INPUTS</span></span>

### <span data-ttu-id="447f4-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="447f4-128">None</span></span>
<span data-ttu-id="447f4-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="447f4-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="447f4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="447f4-130">OUTPUTS</span></span>

### <span data-ttu-id="447f4-131">Booliana</span><span class="sxs-lookup"><span data-stu-id="447f4-131">Boolean</span></span>

## <span data-ttu-id="447f4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="447f4-132">NOTES</span></span>

## <span data-ttu-id="447f4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="447f4-133">RELATED LINKS</span></span>

[<span data-ttu-id="447f4-134">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="447f4-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="447f4-135">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="447f4-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="447f4-136">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="447f4-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="447f4-137">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="447f4-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="447f4-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="447f4-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


