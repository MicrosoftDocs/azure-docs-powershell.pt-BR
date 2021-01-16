---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432775"
---
# <span data-ttu-id="50563-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="50563-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="50563-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50563-102">SYNOPSIS</span></span>
<span data-ttu-id="50563-103">Testa a existência de uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="50563-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="50563-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50563-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50563-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50563-105">DESCRIPTION</span></span>
<span data-ttu-id="50563-106">O cmdlet Test-AzAnalysisServicesServer testa a existência de uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="50563-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="50563-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50563-107">EXAMPLES</span></span>

### <span data-ttu-id="50563-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50563-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="50563-109">Esse comando testará se há um servidor chamado TestServer no botão de teste do MySource</span><span class="sxs-lookup"><span data-stu-id="50563-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="50563-110">OS</span><span class="sxs-lookup"><span data-stu-id="50563-110">PARAMETERS</span></span>

### <span data-ttu-id="50563-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50563-111">-DefaultProfile</span></span>
<span data-ttu-id="50563-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50563-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50563-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="50563-113">-Name</span></span>
<span data-ttu-id="50563-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="50563-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="50563-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50563-115">-ResourceGroupName</span></span>
<span data-ttu-id="50563-116">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="50563-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="50563-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50563-117">CommonParameters</span></span>
<span data-ttu-id="50563-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50563-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50563-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50563-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50563-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50563-120">INPUTS</span></span>

### <span data-ttu-id="50563-121">System. String</span><span class="sxs-lookup"><span data-stu-id="50563-121">System.String</span></span>

## <span data-ttu-id="50563-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50563-122">OUTPUTS</span></span>

### <span data-ttu-id="50563-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50563-123">System.Boolean</span></span>

## <span data-ttu-id="50563-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50563-124">NOTES</span></span>
<span data-ttu-id="50563-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="50563-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="50563-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50563-126">RELATED LINKS</span></span>

[<span data-ttu-id="50563-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="50563-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="50563-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="50563-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
