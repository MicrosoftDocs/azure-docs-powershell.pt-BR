---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601675"
---
# <span data-ttu-id="ab222-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab222-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="ab222-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab222-102">SYNOPSIS</span></span>
<span data-ttu-id="ab222-103">Cria uma instância de PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ab222-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="ab222-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab222-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab222-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab222-105">DESCRIPTION</span></span>
<span data-ttu-id="ab222-106">O cmdlet **New-AzApiManagementContext** cria uma instância de **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ab222-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="ab222-107">O contexto é usado para todos os cmdlets do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ab222-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="ab222-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab222-108">EXAMPLES</span></span>

### <span data-ttu-id="ab222-109">Exemplo 1: criar uma instância de PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab222-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="ab222-110">Esse comando cria uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ab222-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="ab222-111">OS</span><span class="sxs-lookup"><span data-stu-id="ab222-111">PARAMETERS</span></span>

### <span data-ttu-id="ab222-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab222-112">-DefaultProfile</span></span>
<span data-ttu-id="ab222-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab222-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab222-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab222-114">-ResourceGroupName</span></span>
<span data-ttu-id="ab222-115">Especifica o nome do grupo de recursos sob o qual um serviço de gerenciamento de API é implantado.</span><span class="sxs-lookup"><span data-stu-id="ab222-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="ab222-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ab222-116">-ServiceName</span></span>
<span data-ttu-id="ab222-117">Especifica o nome do serviço de gerenciamento de API implantado.</span><span class="sxs-lookup"><span data-stu-id="ab222-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="ab222-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab222-118">CommonParameters</span></span>
<span data-ttu-id="ab222-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab222-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab222-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab222-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab222-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab222-121">INPUTS</span></span>

### <span data-ttu-id="ab222-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ab222-122">System.String</span></span>

## <span data-ttu-id="ab222-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab222-123">OUTPUTS</span></span>

### <span data-ttu-id="ab222-124">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab222-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="ab222-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab222-125">NOTES</span></span>

## <span data-ttu-id="ab222-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab222-126">RELATED LINKS</span></span>
