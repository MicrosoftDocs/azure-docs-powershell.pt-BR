---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440897"
---
# <span data-ttu-id="d1a3e-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d1a3e-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="d1a3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a3e-103">Remove um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1a3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a3e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a3e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a3e-106">O cmdlet **Remove-AzureRmApiManagementAuthorizationServer** remove um servidor de autorização de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="d1a3e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1a3e-107">EXAMPLES</span></span>

## <span data-ttu-id="d1a3e-108">OS</span><span class="sxs-lookup"><span data-stu-id="d1a3e-108">PARAMETERS</span></span>

### <span data-ttu-id="d1a3e-109">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d1a3e-109">-Context</span></span>
<span data-ttu-id="d1a3e-110">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d1a3e-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1a3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a3e-111">-DefaultProfile</span></span>
<span data-ttu-id="d1a3e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d1a3e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1a3e-113">-PassThru</span></span>
<span data-ttu-id="d1a3e-114">PassThru</span><span class="sxs-lookup"><span data-stu-id="d1a3e-114">passthru</span></span>

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

### <span data-ttu-id="d1a3e-115">-ServerID</span><span class="sxs-lookup"><span data-stu-id="d1a3e-115">-ServerId</span></span>
<span data-ttu-id="d1a3e-116">Especifica a ID do servidor de autorização a ser removida.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="d1a3e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1a3e-117">-Confirm</span></span>
<span data-ttu-id="d1a3e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a3e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a3e-119">-WhatIf</span></span>
<span data-ttu-id="d1a3e-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a3e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a3e-122">CommonParameters</span></span>
<span data-ttu-id="d1a3e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a3e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a3e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a3e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1a3e-125">INPUTS</span></span>

### <span data-ttu-id="d1a3e-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d1a3e-126">None</span></span>
<span data-ttu-id="d1a3e-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1a3e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1a3e-128">OUTPUTS</span></span>

### <span data-ttu-id="d1a3e-129">Booliana</span><span class="sxs-lookup"><span data-stu-id="d1a3e-129">Boolean</span></span>

## <span data-ttu-id="d1a3e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1a3e-130">NOTES</span></span>

## <span data-ttu-id="d1a3e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1a3e-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1a3e-132">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d1a3e-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="d1a3e-133">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d1a3e-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="d1a3e-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d1a3e-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


