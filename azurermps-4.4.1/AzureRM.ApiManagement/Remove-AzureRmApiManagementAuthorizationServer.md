---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427033"
---
# <span data-ttu-id="1b3c9-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1b3c9-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1b3c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3c9-103">Remove um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b3c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b3c9-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b3c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="1b3c9-106">O cmdlet **Remove-AzureRmApiManagementAuthorizationServer** remove um servidor de autorização de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="1b3c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b3c9-107">EXAMPLES</span></span>

## <span data-ttu-id="1b3c9-108">OS</span><span class="sxs-lookup"><span data-stu-id="1b3c9-108">PARAMETERS</span></span>

### <span data-ttu-id="1b3c9-109">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1b3c9-109">-Context</span></span>
<span data-ttu-id="1b3c9-110">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1b3c9-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b3c9-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b3c9-111">-PassThru</span></span>
<span data-ttu-id="1b3c9-112">PassThru</span><span class="sxs-lookup"><span data-stu-id="1b3c9-112">passthru</span></span>

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

### <span data-ttu-id="1b3c9-113">-ServerID</span><span class="sxs-lookup"><span data-stu-id="1b3c9-113">-ServerId</span></span>
<span data-ttu-id="1b3c9-114">Especifica a ID do servidor de autorização a ser removida.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="1b3c9-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b3c9-115">-Confirm</span></span>
<span data-ttu-id="1b3c9-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b3c9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b3c9-117">-WhatIf</span></span>
<span data-ttu-id="1b3c9-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b3c9-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b3c9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3c9-120">-DefaultProfile</span></span>
<span data-ttu-id="1b3c9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b3c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3c9-122">CommonParameters</span></span>
<span data-ttu-id="1b3c9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3c9-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b3c9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3c9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b3c9-125">INPUTS</span></span>

## <span data-ttu-id="1b3c9-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b3c9-126">OUTPUTS</span></span>

### <span data-ttu-id="1b3c9-127">Booliana</span><span class="sxs-lookup"><span data-stu-id="1b3c9-127">Boolean</span></span>

## <span data-ttu-id="1b3c9-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b3c9-128">NOTES</span></span>

## <span data-ttu-id="1b3c9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b3c9-129">RELATED LINKS</span></span>

[<span data-ttu-id="1b3c9-130">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1b3c9-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="1b3c9-131">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1b3c9-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="1b3c9-132">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1b3c9-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


