---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426502"
---
# <span data-ttu-id="7598b-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7598b-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7598b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7598b-102">SYNOPSIS</span></span>
<span data-ttu-id="7598b-103">Remove um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="7598b-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7598b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7598b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7598b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7598b-105">DESCRIPTION</span></span>
<span data-ttu-id="7598b-106">O cmdlet **Remove-AzureRmApiManagementAuthorizationServer** remove um servidor de autorização de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="7598b-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="7598b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7598b-107">EXAMPLES</span></span>

## <span data-ttu-id="7598b-108">OS</span><span class="sxs-lookup"><span data-stu-id="7598b-108">PARAMETERS</span></span>

### <span data-ttu-id="7598b-109">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7598b-109">-Context</span></span>
<span data-ttu-id="7598b-110">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7598b-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7598b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7598b-111">-DefaultProfile</span></span>
<span data-ttu-id="7598b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7598b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7598b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7598b-113">-PassThru</span></span>
<span data-ttu-id="7598b-114">PassThru</span><span class="sxs-lookup"><span data-stu-id="7598b-114">passthru</span></span>

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

### <span data-ttu-id="7598b-115">-ServerID</span><span class="sxs-lookup"><span data-stu-id="7598b-115">-ServerId</span></span>
<span data-ttu-id="7598b-116">Especifica a ID do servidor de autorização a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7598b-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="7598b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7598b-117">-Confirm</span></span>
<span data-ttu-id="7598b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7598b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7598b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7598b-119">-WhatIf</span></span>
<span data-ttu-id="7598b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7598b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7598b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7598b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7598b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7598b-122">CommonParameters</span></span>
<span data-ttu-id="7598b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7598b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7598b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7598b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7598b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7598b-125">INPUTS</span></span>

### <span data-ttu-id="7598b-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7598b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7598b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7598b-127">System.String</span></span>

### <span data-ttu-id="7598b-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7598b-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7598b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7598b-129">OUTPUTS</span></span>

### <span data-ttu-id="7598b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7598b-130">System.Boolean</span></span>

## <span data-ttu-id="7598b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7598b-131">NOTES</span></span>

## <span data-ttu-id="7598b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7598b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7598b-133">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7598b-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7598b-134">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7598b-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7598b-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7598b-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


