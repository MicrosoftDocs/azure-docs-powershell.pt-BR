---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110663"
---
# <span data-ttu-id="cd88e-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cd88e-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="cd88e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd88e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd88e-103">Cria uma instância de **PsApiManagementHttpMessageDiagnostic** que é uma configuração de diagnóstico de mensagem http do diagnóstico</span><span class="sxs-lookup"><span data-stu-id="cd88e-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="cd88e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd88e-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd88e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd88e-105">DESCRIPTION</span></span>
<span data-ttu-id="cd88e-106">O cmdlet **New-AzApiManagementHttpMessageDiagnostic** cria a configuração de diagnóstico de mensagem http.</span><span class="sxs-lookup"><span data-stu-id="cd88e-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="cd88e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd88e-107">EXAMPLES</span></span>

### <span data-ttu-id="cd88e-108">Exemplo 1: criar uma configuração básica de diagnóstico de mensagem http</span><span class="sxs-lookup"><span data-stu-id="cd88e-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="cd88e-109">Crie uma configuração de diagnóstico de mensagem http para criar um log `Content-Type` e `User-Agent` cabeçalhos com 100 bytes de `body`</span><span class="sxs-lookup"><span data-stu-id="cd88e-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="cd88e-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd88e-110">PARAMETERS</span></span>

### <span data-ttu-id="cd88e-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="cd88e-111">-BodyBytesToLog</span></span>
<span data-ttu-id="cd88e-112">Número de bytes do corpo da solicitação a serem registradas.</span><span class="sxs-lookup"><span data-stu-id="cd88e-112">Number of request body bytes to log.</span></span> <span data-ttu-id="cd88e-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cd88e-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd88e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd88e-114">-DefaultProfile</span></span>
<span data-ttu-id="cd88e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd88e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd88e-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="cd88e-116">-HeadersToLog</span></span>
<span data-ttu-id="cd88e-117">A matriz de cabeçalhos a serem registradas.</span><span class="sxs-lookup"><span data-stu-id="cd88e-117">The array of headers to log.</span></span> <span data-ttu-id="cd88e-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cd88e-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd88e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd88e-119">CommonParameters</span></span>
<span data-ttu-id="cd88e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd88e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd88e-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd88e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd88e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd88e-122">INPUTS</span></span>

### <span data-ttu-id="cd88e-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cd88e-123">None</span></span>

## <span data-ttu-id="cd88e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd88e-124">OUTPUTS</span></span>

### <span data-ttu-id="cd88e-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cd88e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="cd88e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd88e-126">NOTES</span></span>

## <span data-ttu-id="cd88e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd88e-127">RELATED LINKS</span></span>

[<span data-ttu-id="cd88e-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cd88e-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cd88e-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="cd88e-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)