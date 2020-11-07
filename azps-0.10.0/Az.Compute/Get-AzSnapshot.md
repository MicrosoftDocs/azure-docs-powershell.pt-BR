---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777052"
---
# <span data-ttu-id="8bfca-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="8bfca-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="8bfca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bfca-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfca-103">Obtém as propriedades de um instantâneo</span><span class="sxs-lookup"><span data-stu-id="8bfca-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="8bfca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bfca-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bfca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bfca-105">DESCRIPTION</span></span>
<span data-ttu-id="8bfca-106">O cmdlet **Get-AzSnapshot** Obtém as propriedades de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8bfca-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="8bfca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bfca-107">EXAMPLES</span></span>

### <span data-ttu-id="8bfca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bfca-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="8bfca-109">Este comando obtém as propriedades de todos os instantâneos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8bfca-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="8bfca-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8bfca-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="8bfca-111">Esse comando obtém as propriedades de todos os instantâneos no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="8bfca-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="8bfca-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8bfca-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="8bfca-113">Este comando obtém as propriedades do instantâneo chamado "SnapshotName1" no grupo de recursos chamado "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="8bfca-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="8bfca-114">OS</span><span class="sxs-lookup"><span data-stu-id="8bfca-114">PARAMETERS</span></span>

### <span data-ttu-id="8bfca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfca-115">-DefaultProfile</span></span>
<span data-ttu-id="8bfca-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bfca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bfca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bfca-117">-ResourceGroupName</span></span>
<span data-ttu-id="8bfca-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bfca-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8bfca-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="8bfca-119">-SnapshotName</span></span>
<span data-ttu-id="8bfca-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8bfca-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bfca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfca-121">CommonParameters</span></span>
<span data-ttu-id="8bfca-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bfca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfca-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bfca-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfca-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bfca-124">INPUTS</span></span>

### <span data-ttu-id="8bfca-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8bfca-125">System.String</span></span>

## <span data-ttu-id="8bfca-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bfca-126">OUTPUTS</span></span>

### <span data-ttu-id="8bfca-127">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8bfca-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8bfca-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bfca-128">NOTES</span></span>

## <span data-ttu-id="8bfca-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bfca-129">RELATED LINKS</span></span>

