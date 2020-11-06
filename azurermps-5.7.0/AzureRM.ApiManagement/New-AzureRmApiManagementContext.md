---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429910"
---
# <span data-ttu-id="f6834-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f6834-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="f6834-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6834-102">SYNOPSIS</span></span>
<span data-ttu-id="f6834-103">Cria uma instância de PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f6834-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6834-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6834-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6834-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6834-105">DESCRIPTION</span></span>
<span data-ttu-id="f6834-106">O cmdlet **New-AzureRmApiManagementContext** cria uma instância de **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f6834-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="f6834-107">O contexto é usado para todos os cmdlets do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f6834-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="f6834-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6834-108">EXAMPLES</span></span>

### <span data-ttu-id="f6834-109">Exemplo 1: criar uma instância de PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f6834-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="f6834-110">Esse comando cria uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f6834-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="f6834-111">OS</span><span class="sxs-lookup"><span data-stu-id="f6834-111">PARAMETERS</span></span>

### <span data-ttu-id="f6834-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6834-112">-DefaultProfile</span></span>
<span data-ttu-id="f6834-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6834-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6834-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6834-114">-ResourceGroupName</span></span>
<span data-ttu-id="f6834-115">Especifica o nome do grupo de recursos sob o qual um serviço de gerenciamento de API é implantado.</span><span class="sxs-lookup"><span data-stu-id="f6834-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6834-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f6834-116">-ServiceName</span></span>
<span data-ttu-id="f6834-117">Especifica o nome do serviço de gerenciamento de API implantado.</span><span class="sxs-lookup"><span data-stu-id="f6834-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6834-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6834-118">CommonParameters</span></span>
<span data-ttu-id="f6834-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6834-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6834-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6834-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6834-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6834-121">INPUTS</span></span>

### <span data-ttu-id="f6834-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f6834-122">None</span></span>
<span data-ttu-id="f6834-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f6834-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6834-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6834-124">OUTPUTS</span></span>

### <span data-ttu-id="f6834-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f6834-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="f6834-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6834-126">NOTES</span></span>

## <span data-ttu-id="f6834-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6834-127">RELATED LINKS</span></span>

