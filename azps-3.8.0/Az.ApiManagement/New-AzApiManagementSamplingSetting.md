---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 61f046576c14b61a59b55c52dd69c3e72b2c839e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942217"
---
# <span data-ttu-id="0db6b-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="0db6b-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="0db6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0db6b-102">SYNOPSIS</span></span>
<span data-ttu-id="0db6b-103">Criar uma nova configuração de amostragem para o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="0db6b-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="0db6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0db6b-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0db6b-105">DESCRIPTION</span></span>
<span data-ttu-id="0db6b-106">O cmdlet **New-AzApiManagementSamplingSetting** cria uma nova configuração de amostragem para o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="0db6b-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="0db6b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0db6b-107">EXAMPLES</span></span>

### <span data-ttu-id="0db6b-108">Exemplo 1: criar uma configuração de amostragem básica</span><span class="sxs-lookup"><span data-stu-id="0db6b-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="0db6b-109">Cria uma configuração de amostragem do `Fixed` tipo com registro em log para 100% das solicitações/respostas</span><span class="sxs-lookup"><span data-stu-id="0db6b-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="0db6b-110">OS</span><span class="sxs-lookup"><span data-stu-id="0db6b-110">PARAMETERS</span></span>

### <span data-ttu-id="0db6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db6b-111">-DefaultProfile</span></span>
<span data-ttu-id="0db6b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0db6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db6b-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="0db6b-113">-SamplingPercentage</span></span>
<span data-ttu-id="0db6b-114">Taxa de amostragem para amostragem de taxa fixa.</span><span class="sxs-lookup"><span data-stu-id="0db6b-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="0db6b-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0db6b-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db6b-116">-Amostragemtype</span><span class="sxs-lookup"><span data-stu-id="0db6b-116">-SamplingType</span></span>
<span data-ttu-id="0db6b-117">O tipo de amostragem.</span><span class="sxs-lookup"><span data-stu-id="0db6b-117">The Type of Sampling.</span></span>
<span data-ttu-id="0db6b-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0db6b-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="0db6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db6b-119">CommonParameters</span></span>
<span data-ttu-id="0db6b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db6b-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0db6b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db6b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0db6b-122">INPUTS</span></span>

### <span data-ttu-id="0db6b-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0db6b-123">None</span></span>

## <span data-ttu-id="0db6b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0db6b-124">OUTPUTS</span></span>

### <span data-ttu-id="0db6b-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="0db6b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="0db6b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0db6b-126">NOTES</span></span>

## <span data-ttu-id="0db6b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0db6b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0db6b-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0db6b-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0db6b-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0db6b-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0db6b-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0db6b-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0db6b-131">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="0db6b-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
