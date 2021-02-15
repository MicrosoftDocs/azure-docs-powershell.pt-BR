---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118099"
---
# <span data-ttu-id="73fe7-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="73fe7-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="73fe7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="73fe7-103">Testa a existência de uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="73fe7-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="73fe7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73fe7-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73fe7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="73fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="73fe7-106">O Test-AzAnalysisServicesServer cmdlet testa a existência de uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="73fe7-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="73fe7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73fe7-107">EXAMPLES</span></span>

### <span data-ttu-id="73fe7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73fe7-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="73fe7-109">Esse comando testará se há um servidor chamado testserver no grupo de teste de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="73fe7-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="73fe7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73fe7-110">PARAMETERS</span></span>

### <span data-ttu-id="73fe7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fe7-111">-DefaultProfile</span></span>
<span data-ttu-id="73fe7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="73fe7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73fe7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="73fe7-113">-Name</span></span>
<span data-ttu-id="73fe7-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="73fe7-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fe7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fe7-115">-ResourceGroupName</span></span>
<span data-ttu-id="73fe7-116">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="73fe7-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="73fe7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fe7-117">CommonParameters</span></span>
<span data-ttu-id="73fe7-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73fe7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fe7-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73fe7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fe7-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="73fe7-120">INPUTS</span></span>

### <span data-ttu-id="73fe7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="73fe7-121">System.String</span></span>

## <span data-ttu-id="73fe7-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="73fe7-122">OUTPUTS</span></span>

### <span data-ttu-id="73fe7-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73fe7-123">System.Boolean</span></span>

## <span data-ttu-id="73fe7-124">Notas</span><span class="sxs-lookup"><span data-stu-id="73fe7-124">NOTES</span></span>
<span data-ttu-id="73fe7-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="73fe7-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="73fe7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73fe7-126">RELATED LINKS</span></span>

[<span data-ttu-id="73fe7-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="73fe7-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="73fe7-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="73fe7-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
