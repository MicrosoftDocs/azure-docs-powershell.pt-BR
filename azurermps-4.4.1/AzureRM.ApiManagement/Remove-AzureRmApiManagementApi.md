---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427037"
---
# <span data-ttu-id="6b876-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6b876-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="6b876-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b876-102">SYNOPSIS</span></span>
<span data-ttu-id="6b876-103">Remove uma API.</span><span class="sxs-lookup"><span data-stu-id="6b876-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b876-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b876-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b876-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b876-105">DESCRIPTION</span></span>
<span data-ttu-id="6b876-106">O cmdlet **Remove-AzureRmApiManagementApi** remove uma API existente.</span><span class="sxs-lookup"><span data-stu-id="6b876-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="6b876-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b876-107">EXAMPLES</span></span>

### <span data-ttu-id="6b876-108">Exemplo 1: remover uma API</span><span class="sxs-lookup"><span data-stu-id="6b876-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="6b876-109">Este comando Remove a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="6b876-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="6b876-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b876-110">PARAMETERS</span></span>

### <span data-ttu-id="6b876-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6b876-111">-ApiId</span></span>
<span data-ttu-id="6b876-112">Especifica a ID da API remove.</span><span class="sxs-lookup"><span data-stu-id="6b876-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="6b876-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6b876-113">-Context</span></span>
<span data-ttu-id="6b876-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6b876-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6b876-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b876-115">-PassThru</span></span>
<span data-ttu-id="6b876-116">PassThru</span><span class="sxs-lookup"><span data-stu-id="6b876-116">passthru</span></span>

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

### <span data-ttu-id="6b876-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b876-117">-Confirm</span></span>
<span data-ttu-id="6b876-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b876-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b876-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b876-119">-WhatIf</span></span>
<span data-ttu-id="6b876-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b876-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b876-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b876-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b876-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b876-122">-DefaultProfile</span></span>
<span data-ttu-id="6b876-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b876-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b876-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b876-124">CommonParameters</span></span>
<span data-ttu-id="6b876-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b876-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b876-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b876-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b876-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b876-127">INPUTS</span></span>

## <span data-ttu-id="6b876-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b876-128">OUTPUTS</span></span>

### <span data-ttu-id="6b876-129">Booliana</span><span class="sxs-lookup"><span data-stu-id="6b876-129">Boolean</span></span>

## <span data-ttu-id="6b876-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b876-130">NOTES</span></span>

## <span data-ttu-id="6b876-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b876-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b876-132">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6b876-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="6b876-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6b876-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="6b876-134">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6b876-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="6b876-135">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6b876-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="6b876-136">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6b876-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


