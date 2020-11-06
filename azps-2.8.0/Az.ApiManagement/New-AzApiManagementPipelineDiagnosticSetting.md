---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: f2d9c12cb3795d23144fa5296cba992a25383819
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598034"
---
# <span data-ttu-id="cf24a-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cf24a-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="cf24a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf24a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf24a-103">Crie configurações de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="cf24a-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="cf24a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf24a-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf24a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf24a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf24a-106">O cmdlet **New-AzApiManagementPipelineDiagnosticSetting** cria as configurações de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="cf24a-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="cf24a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf24a-107">EXAMPLES</span></span>

### <span data-ttu-id="cf24a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf24a-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="cf24a-109">Crie um diagnóstico de pipeline para ser usado em front-end ou backend na entidade de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="cf24a-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="cf24a-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf24a-110">PARAMETERS</span></span>

### <span data-ttu-id="cf24a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf24a-111">-DefaultProfile</span></span>
<span data-ttu-id="cf24a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf24a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf24a-113">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="cf24a-113">-Request</span></span>
<span data-ttu-id="cf24a-114">Configuração de diagnóstico para solicitação.</span><span class="sxs-lookup"><span data-stu-id="cf24a-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="cf24a-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cf24a-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf24a-116">-Resposta</span><span class="sxs-lookup"><span data-stu-id="cf24a-116">-Response</span></span>
<span data-ttu-id="cf24a-117">Configuração de diagnóstico para resposta.</span><span class="sxs-lookup"><span data-stu-id="cf24a-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="cf24a-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cf24a-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf24a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf24a-119">CommonParameters</span></span>
<span data-ttu-id="cf24a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf24a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf24a-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf24a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf24a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf24a-122">INPUTS</span></span>

### <span data-ttu-id="cf24a-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cf24a-123">None</span></span>

## <span data-ttu-id="cf24a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf24a-124">OUTPUTS</span></span>

### <span data-ttu-id="cf24a-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cf24a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="cf24a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf24a-126">NOTES</span></span>

## <span data-ttu-id="cf24a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf24a-127">RELATED LINKS</span></span>

[<span data-ttu-id="cf24a-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cf24a-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cf24a-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cf24a-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cf24a-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cf24a-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cf24a-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cf24a-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


