---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256647"
---
# <span data-ttu-id="96e20-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="96e20-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="96e20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96e20-102">SYNOPSIS</span></span>
<span data-ttu-id="96e20-103">Obtém os detalhes de um servidor do Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="96e20-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="96e20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96e20-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96e20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96e20-105">DESCRIPTION</span></span>
<span data-ttu-id="96e20-106">O cmdlet Get-AzAnalysisServicesServer Obtém os detalhes de um servidor do Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="96e20-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="96e20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96e20-107">EXAMPLES</span></span>

### <span data-ttu-id="96e20-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96e20-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="96e20-109">Esse comando obtém todos os servidores do Azure Analysis Services no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="96e20-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="96e20-110">Exemplo 2: obter um servidor</span><span class="sxs-lookup"><span data-stu-id="96e20-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="96e20-111">Esse comando obtém o servidor do Azure Analysis Services chamado TestServer no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="96e20-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="96e20-112">OS</span><span class="sxs-lookup"><span data-stu-id="96e20-112">PARAMETERS</span></span>

### <span data-ttu-id="96e20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e20-113">-DefaultProfile</span></span>
<span data-ttu-id="96e20-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96e20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96e20-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="96e20-115">-Name</span></span>
<span data-ttu-id="96e20-116">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="96e20-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="96e20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e20-117">-ResourceGroupName</span></span>
<span data-ttu-id="96e20-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="96e20-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="96e20-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e20-119">CommonParameters</span></span>
<span data-ttu-id="96e20-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e20-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e20-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e20-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e20-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96e20-122">INPUTS</span></span>

### <span data-ttu-id="96e20-123">System. String</span><span class="sxs-lookup"><span data-stu-id="96e20-123">System.String</span></span>

## <span data-ttu-id="96e20-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96e20-124">OUTPUTS</span></span>

### <span data-ttu-id="96e20-125">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="96e20-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="96e20-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96e20-126">NOTES</span></span>
<span data-ttu-id="96e20-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="96e20-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="96e20-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96e20-128">RELATED LINKS</span></span>

[<span data-ttu-id="96e20-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="96e20-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="96e20-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="96e20-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
