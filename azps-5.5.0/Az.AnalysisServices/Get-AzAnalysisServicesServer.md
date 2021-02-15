---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114862"
---
# <span data-ttu-id="1d209-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1d209-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="1d209-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d209-102">SYNOPSIS</span></span>
<span data-ttu-id="1d209-103">Obtém os detalhes de um servidor do Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="1d209-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="1d209-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d209-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d209-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d209-105">DESCRIPTION</span></span>
<span data-ttu-id="1d209-106">O Get-AzAnalysisServicesServer cmdlet obtém os detalhes de um servidor do Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="1d209-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="1d209-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1d209-107">EXAMPLES</span></span>

### <span data-ttu-id="1d209-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d209-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="1d209-109">Esse comando obtém todos os servidores do Azure Analysis Services no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="1d209-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="1d209-110">Exemplo 2: Obter um servidor</span><span class="sxs-lookup"><span data-stu-id="1d209-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="1d209-111">Esse comando obtém o servidor do Azure Analysis Services chamado de testserver no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="1d209-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="1d209-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d209-112">PARAMETERS</span></span>

### <span data-ttu-id="1d209-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d209-113">-DefaultProfile</span></span>
<span data-ttu-id="1d209-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1d209-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d209-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d209-115">-Name</span></span>
<span data-ttu-id="1d209-116">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1d209-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="1d209-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d209-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d209-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="1d209-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="1d209-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d209-119">CommonParameters</span></span>
<span data-ttu-id="1d209-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d209-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d209-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d209-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d209-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="1d209-122">INPUTS</span></span>

### <span data-ttu-id="1d209-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1d209-123">System.String</span></span>

## <span data-ttu-id="1d209-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="1d209-124">OUTPUTS</span></span>

### <span data-ttu-id="1d209-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1d209-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="1d209-126">Notas</span><span class="sxs-lookup"><span data-stu-id="1d209-126">NOTES</span></span>
<span data-ttu-id="1d209-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="1d209-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="1d209-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d209-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d209-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="1d209-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="1d209-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="1d209-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
