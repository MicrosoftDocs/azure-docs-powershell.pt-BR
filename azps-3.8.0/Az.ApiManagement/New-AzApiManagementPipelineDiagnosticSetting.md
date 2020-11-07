---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942222"
---
# <span data-ttu-id="72bd5-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="72bd5-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="72bd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="72bd5-103">Crie configurações de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="72bd5-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="72bd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72bd5-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72bd5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="72bd5-106">O cmdlet **New-AzApiManagementPipelineDiagnosticSetting** cria as configurações de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="72bd5-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="72bd5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72bd5-107">EXAMPLES</span></span>

### <span data-ttu-id="72bd5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72bd5-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="72bd5-109">Crie um diagnóstico de pipeline para ser usado em front-end ou backend na entidade de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="72bd5-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="72bd5-110">OS</span><span class="sxs-lookup"><span data-stu-id="72bd5-110">PARAMETERS</span></span>

### <span data-ttu-id="72bd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bd5-111">-DefaultProfile</span></span>
<span data-ttu-id="72bd5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72bd5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72bd5-113">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="72bd5-113">-Request</span></span>
<span data-ttu-id="72bd5-114">Configuração de diagnóstico para solicitação.</span><span class="sxs-lookup"><span data-stu-id="72bd5-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="72bd5-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="72bd5-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bd5-116">-Resposta</span><span class="sxs-lookup"><span data-stu-id="72bd5-116">-Response</span></span>
<span data-ttu-id="72bd5-117">Configuração de diagnóstico para resposta.</span><span class="sxs-lookup"><span data-stu-id="72bd5-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="72bd5-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="72bd5-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bd5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bd5-119">CommonParameters</span></span>
<span data-ttu-id="72bd5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72bd5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bd5-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72bd5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bd5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72bd5-122">INPUTS</span></span>

### <span data-ttu-id="72bd5-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="72bd5-123">None</span></span>

## <span data-ttu-id="72bd5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72bd5-124">OUTPUTS</span></span>

### <span data-ttu-id="72bd5-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="72bd5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="72bd5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72bd5-126">NOTES</span></span>

## <span data-ttu-id="72bd5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72bd5-127">RELATED LINKS</span></span>

[<span data-ttu-id="72bd5-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="72bd5-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="72bd5-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="72bd5-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="72bd5-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="72bd5-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="72bd5-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="72bd5-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


