---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: efd4c4770bb9a2628530f476d44e9774534ceee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429623"
---
# <span data-ttu-id="18759-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="18759-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="18759-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18759-102">SYNOPSIS</span></span>
<span data-ttu-id="18759-103">Obtém os detalhes de um servidor do Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="18759-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18759-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18759-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18759-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18759-105">DESCRIPTION</span></span>
<span data-ttu-id="18759-106">O cmdlet Get-AzureRmAnalysisServicesServer Obtém os detalhes de um servidor do Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="18759-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="18759-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18759-107">EXAMPLES</span></span>

### <span data-ttu-id="18759-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18759-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="18759-109">Esse comando obtém todos os servidores do Azure Analysis Services no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="18759-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="18759-110">Exemplo 2: obter um servidor</span><span class="sxs-lookup"><span data-stu-id="18759-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="18759-111">Esse comando obtém o servidor do Azure Analysis Services chamado TestServer no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="18759-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="18759-112">OS</span><span class="sxs-lookup"><span data-stu-id="18759-112">PARAMETERS</span></span>

### <span data-ttu-id="18759-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18759-113">-DefaultProfile</span></span>
<span data-ttu-id="18759-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18759-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18759-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="18759-115">-Name</span></span>
<span data-ttu-id="18759-116">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="18759-116">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18759-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18759-117">-ResourceGroupName</span></span>
<span data-ttu-id="18759-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="18759-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18759-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18759-119">CommonParameters</span></span>
<span data-ttu-id="18759-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18759-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18759-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18759-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18759-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18759-122">INPUTS</span></span>

### <span data-ttu-id="18759-123">System. String</span><span class="sxs-lookup"><span data-stu-id="18759-123">System.String</span></span>

## <span data-ttu-id="18759-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18759-124">OUTPUTS</span></span>

### <span data-ttu-id="18759-125">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="18759-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="18759-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18759-126">NOTES</span></span>
<span data-ttu-id="18759-127">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="18759-127">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="18759-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18759-128">RELATED LINKS</span></span>

[<span data-ttu-id="18759-129">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="18759-129">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="18759-130">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="18759-130">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
