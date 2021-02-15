---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114993"
---
# <span data-ttu-id="4650b-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4650b-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4650b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4650b-102">SYNOPSIS</span></span>
<span data-ttu-id="4650b-103">Testa a existência de uma instância de Capacidade Inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4650b-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4650b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4650b-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4650b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4650b-105">DESCRIPTION</span></span>
<span data-ttu-id="4650b-106">O Test-AzPowerBIEmbeddedCapacity cmdlet testa a existência de uma instância de Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="4650b-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4650b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4650b-107">EXAMPLES</span></span>

### <span data-ttu-id="4650b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4650b-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="4650b-109">Esse comando testará se há uma capacidade chamada testcapacity</span><span class="sxs-lookup"><span data-stu-id="4650b-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="4650b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4650b-110">PARAMETERS</span></span>

### <span data-ttu-id="4650b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4650b-111">-DefaultProfile</span></span>
<span data-ttu-id="4650b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4650b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4650b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4650b-113">-Name</span></span>
<span data-ttu-id="4650b-114">Nome da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="4650b-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4650b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4650b-115">CommonParameters</span></span>
<span data-ttu-id="4650b-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4650b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4650b-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4650b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4650b-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="4650b-118">INPUTS</span></span>

### <span data-ttu-id="4650b-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4650b-119">None</span></span>

## <span data-ttu-id="4650b-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="4650b-120">OUTPUTS</span></span>

### <span data-ttu-id="4650b-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4650b-121">System.Boolean</span></span>

## <span data-ttu-id="4650b-122">Notas</span><span class="sxs-lookup"><span data-stu-id="4650b-122">NOTES</span></span>

## <span data-ttu-id="4650b-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4650b-123">RELATED LINKS</span></span>

[<span data-ttu-id="4650b-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4650b-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4650b-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4650b-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
