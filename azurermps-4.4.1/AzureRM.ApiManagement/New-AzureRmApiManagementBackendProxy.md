---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431230"
---
# <span data-ttu-id="a6734-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a6734-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="a6734-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6734-102">SYNOPSIS</span></span>
<span data-ttu-id="a6734-103">Cria um novo objeto proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="a6734-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6734-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6734-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6734-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6734-105">DESCRIPTION</span></span>
<span data-ttu-id="a6734-106">Cria um novo objeto de proxy de back-end que pode ser canalizado ao criar uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="a6734-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="a6734-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6734-107">EXAMPLES</span></span>

### <span data-ttu-id="a6734-108">Criar um objeto de In-Memory proxy de back-end</span><span class="sxs-lookup"><span data-stu-id="a6734-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="a6734-109">Cria um objeto proxy de back-end</span><span class="sxs-lookup"><span data-stu-id="a6734-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="a6734-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6734-110">PARAMETERS</span></span>

### <span data-ttu-id="a6734-111">-Senha</span><span class="sxs-lookup"><span data-stu-id="a6734-111">-Password</span></span>
<span data-ttu-id="a6734-112">Senha do proxy usada para conectar-se ao proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="a6734-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="a6734-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a6734-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6734-114">-URL</span><span class="sxs-lookup"><span data-stu-id="a6734-114">-Url</span></span>
<span data-ttu-id="a6734-115">URL do servidor proxy a ser usado ao encaminhar chamadas para backend.</span><span class="sxs-lookup"><span data-stu-id="a6734-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="a6734-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a6734-116">This parameter is required.</span></span>

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

### <span data-ttu-id="a6734-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="a6734-117">-UserName</span></span>
<span data-ttu-id="a6734-118">Nome de usuário proxy usado para se conectar ao proxy de back-end.</span><span class="sxs-lookup"><span data-stu-id="a6734-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="a6734-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a6734-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6734-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6734-120">-DefaultProfile</span></span>
<span data-ttu-id="a6734-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6734-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6734-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6734-122">CommonParameters</span></span>
<span data-ttu-id="a6734-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6734-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6734-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6734-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6734-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6734-125">INPUTS</span></span>

## <span data-ttu-id="a6734-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6734-126">OUTPUTS</span></span>

### <span data-ttu-id="a6734-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a6734-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="a6734-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6734-128">NOTES</span></span>

## <span data-ttu-id="a6734-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6734-129">RELATED LINKS</span></span>

[<span data-ttu-id="a6734-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a6734-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a6734-131">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a6734-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a6734-132">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a6734-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a6734-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a6734-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a6734-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a6734-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
