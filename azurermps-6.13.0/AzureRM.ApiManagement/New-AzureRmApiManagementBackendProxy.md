---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428643"
---
# <span data-ttu-id="66097-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="66097-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="66097-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66097-102">SYNOPSIS</span></span>
<span data-ttu-id="66097-103">Cria um novo objeto proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="66097-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66097-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66097-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66097-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66097-105">DESCRIPTION</span></span>
<span data-ttu-id="66097-106">Cria um novo objeto de proxy de back-end que pode ser canalizado ao criar uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="66097-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="66097-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66097-107">EXAMPLES</span></span>

### <span data-ttu-id="66097-108">Criar um objeto de In-Memory proxy de back-end</span><span class="sxs-lookup"><span data-stu-id="66097-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="66097-109">Cria um objeto proxy de back-end e configura o back-end</span><span class="sxs-lookup"><span data-stu-id="66097-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="66097-110">OS</span><span class="sxs-lookup"><span data-stu-id="66097-110">PARAMETERS</span></span>

### <span data-ttu-id="66097-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66097-111">-DefaultProfile</span></span>
<span data-ttu-id="66097-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66097-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66097-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="66097-113">-ProxyCredential</span></span>
<span data-ttu-id="66097-114">Credenciais usadas para se conectar ao proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="66097-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="66097-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="66097-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66097-116">-URL</span><span class="sxs-lookup"><span data-stu-id="66097-116">-Url</span></span>
<span data-ttu-id="66097-117">URL do servidor proxy a ser usado ao encaminhar chamadas para backend.</span><span class="sxs-lookup"><span data-stu-id="66097-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="66097-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="66097-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66097-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66097-119">CommonParameters</span></span>
<span data-ttu-id="66097-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66097-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66097-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66097-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66097-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66097-122">INPUTS</span></span>

### <span data-ttu-id="66097-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="66097-123">None</span></span>

## <span data-ttu-id="66097-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66097-124">OUTPUTS</span></span>

### <span data-ttu-id="66097-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="66097-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="66097-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66097-126">NOTES</span></span>

## <span data-ttu-id="66097-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66097-127">RELATED LINKS</span></span>

[<span data-ttu-id="66097-128">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66097-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="66097-129">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66097-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="66097-130">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="66097-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="66097-131">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66097-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="66097-132">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66097-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
