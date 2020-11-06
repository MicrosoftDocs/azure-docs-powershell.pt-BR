---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440905"
---
# <span data-ttu-id="76352-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="76352-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="76352-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76352-102">SYNOPSIS</span></span>
<span data-ttu-id="76352-103">Testa a existência de uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="76352-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76352-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76352-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76352-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76352-105">DESCRIPTION</span></span>
<span data-ttu-id="76352-106">O cmdlet Test-AzureRmAnalysisServicesServer testa a existência de uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="76352-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="76352-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76352-107">EXAMPLES</span></span>

### <span data-ttu-id="76352-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76352-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="76352-109">Esse comando testará se há um servidor chamado TestServer no botão de teste do MySource</span><span class="sxs-lookup"><span data-stu-id="76352-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="76352-110">OS</span><span class="sxs-lookup"><span data-stu-id="76352-110">PARAMETERS</span></span>

### <span data-ttu-id="76352-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76352-111">-DefaultProfile</span></span>
<span data-ttu-id="76352-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76352-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76352-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="76352-113">-Name</span></span>
<span data-ttu-id="76352-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="76352-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76352-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76352-115">-ResourceGroupName</span></span>
<span data-ttu-id="76352-116">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="76352-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76352-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76352-117">CommonParameters</span></span>
<span data-ttu-id="76352-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76352-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76352-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76352-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76352-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76352-120">INPUTS</span></span>

### <span data-ttu-id="76352-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76352-121">None</span></span>
<span data-ttu-id="76352-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="76352-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76352-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76352-123">OUTPUTS</span></span>

### <span data-ttu-id="76352-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76352-124">System.Boolean</span></span>

## <span data-ttu-id="76352-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76352-125">NOTES</span></span>
<span data-ttu-id="76352-126">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="76352-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="76352-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76352-127">RELATED LINKS</span></span>

[<span data-ttu-id="76352-128">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="76352-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="76352-129">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="76352-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
