---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: aa681d48330755137b9c9687be6c40adc12295f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595641"
---
# <span data-ttu-id="150f1-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="150f1-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="150f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="150f1-102">SYNOPSIS</span></span>
<span data-ttu-id="150f1-103">Cria um novo objeto proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="150f1-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="150f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="150f1-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="150f1-105">DESCRIPTION</span></span>
<span data-ttu-id="150f1-106">Cria um novo objeto de proxy de back-end que pode ser canalizado ao criar uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="150f1-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="150f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="150f1-107">EXAMPLES</span></span>

### <span data-ttu-id="150f1-108">Criar um objeto de In-Memory proxy de back-end</span><span class="sxs-lookup"><span data-stu-id="150f1-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="150f1-109">Cria um objeto proxy de back-end e configura o back-end</span><span class="sxs-lookup"><span data-stu-id="150f1-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="150f1-110">OS</span><span class="sxs-lookup"><span data-stu-id="150f1-110">PARAMETERS</span></span>

### <span data-ttu-id="150f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150f1-111">-DefaultProfile</span></span>
<span data-ttu-id="150f1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="150f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150f1-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="150f1-113">-ProxyCredential</span></span>
<span data-ttu-id="150f1-114">Credenciais usadas para se conectar ao proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="150f1-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="150f1-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="150f1-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="150f1-116">-URL</span><span class="sxs-lookup"><span data-stu-id="150f1-116">-Url</span></span>
<span data-ttu-id="150f1-117">URL do servidor proxy a ser usado ao encaminhar chamadas para backend.</span><span class="sxs-lookup"><span data-stu-id="150f1-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="150f1-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="150f1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="150f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150f1-119">CommonParameters</span></span>
<span data-ttu-id="150f1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150f1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="150f1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150f1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="150f1-122">INPUTS</span></span>

### <span data-ttu-id="150f1-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="150f1-123">None</span></span>

## <span data-ttu-id="150f1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="150f1-124">OUTPUTS</span></span>

### <span data-ttu-id="150f1-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="150f1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="150f1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="150f1-126">NOTES</span></span>

## <span data-ttu-id="150f1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="150f1-127">RELATED LINKS</span></span>

[<span data-ttu-id="150f1-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="150f1-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="150f1-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="150f1-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="150f1-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="150f1-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="150f1-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="150f1-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="150f1-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="150f1-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
