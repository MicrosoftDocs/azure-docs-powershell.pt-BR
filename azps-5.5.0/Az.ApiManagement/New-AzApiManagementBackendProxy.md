---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118055"
---
# <span data-ttu-id="ad920-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ad920-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="ad920-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad920-102">SYNOPSIS</span></span>
<span data-ttu-id="ad920-103">Cria um novo Objeto Proxy back-end.</span><span class="sxs-lookup"><span data-stu-id="ad920-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="ad920-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad920-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad920-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad920-105">DESCRIPTION</span></span>
<span data-ttu-id="ad920-106">Cria um novo Objeto Proxy back-end que pode ser canalado ao criar uma nova entidade Backend.</span><span class="sxs-lookup"><span data-stu-id="ad920-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="ad920-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad920-107">EXAMPLES</span></span>

### <span data-ttu-id="ad920-108">Exemplo 1: Criar um Objeto proxy back-In-Memory Backend</span><span class="sxs-lookup"><span data-stu-id="ad920-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="ad920-109">Cria um Objeto Proxy back-end e configura o Backend</span><span class="sxs-lookup"><span data-stu-id="ad920-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="ad920-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad920-110">PARAMETERS</span></span>

### <span data-ttu-id="ad920-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad920-111">-DefaultProfile</span></span>
<span data-ttu-id="ad920-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ad920-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad920-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="ad920-113">-ProxyCredential</span></span>
<span data-ttu-id="ad920-114">Credenciais usadas para se conectar ao Proxy Backend.</span><span class="sxs-lookup"><span data-stu-id="ad920-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="ad920-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ad920-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad920-116">-Url</span><span class="sxs-lookup"><span data-stu-id="ad920-116">-Url</span></span>
<span data-ttu-id="ad920-117">URL do servidor Proxy a ser usada ao encaminhar chamadas para Backend.</span><span class="sxs-lookup"><span data-stu-id="ad920-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="ad920-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="ad920-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ad920-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad920-119">CommonParameters</span></span>
<span data-ttu-id="ad920-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad920-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad920-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad920-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad920-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="ad920-122">INPUTS</span></span>

### <span data-ttu-id="ad920-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ad920-123">None</span></span>

## <span data-ttu-id="ad920-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="ad920-124">OUTPUTS</span></span>

### <span data-ttu-id="ad920-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ad920-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="ad920-126">Notas</span><span class="sxs-lookup"><span data-stu-id="ad920-126">NOTES</span></span>

## <span data-ttu-id="ad920-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad920-127">RELATED LINKS</span></span>

[<span data-ttu-id="ad920-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad920-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="ad920-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad920-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ad920-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ad920-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ad920-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad920-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ad920-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad920-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
