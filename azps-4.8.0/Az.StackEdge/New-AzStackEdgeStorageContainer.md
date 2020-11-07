---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947535"
---
# <span data-ttu-id="3d835-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d835-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="3d835-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d835-102">SYNOPSIS</span></span>
<span data-ttu-id="3d835-103">Cria um novo contêiner de armazenamento na conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d835-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="3d835-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d835-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d835-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d835-105">DESCRIPTION</span></span>
<span data-ttu-id="3d835-106">O cmdlet **New-AzStackEdgeStorageContainer** cria um novo contêiner de armazenamento na conta de armazenamento de borda em um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="3d835-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="3d835-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d835-107">EXAMPLES</span></span>

### <span data-ttu-id="3d835-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d835-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="3d835-109">OS</span><span class="sxs-lookup"><span data-stu-id="3d835-109">PARAMETERS</span></span>

### <span data-ttu-id="3d835-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d835-110">-AsJob</span></span>
<span data-ttu-id="3d835-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3d835-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-112">-Formato DataFormat</span><span class="sxs-lookup"><span data-stu-id="3d835-112">-DataFormat</span></span>
<span data-ttu-id="3d835-113">Definir formato de dados por exemplo: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="3d835-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d835-114">-DefaultProfile</span></span>
<span data-ttu-id="3d835-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d835-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d835-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3d835-116">-DeviceName</span></span>
<span data-ttu-id="3d835-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d835-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3d835-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="3d835-119">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="3d835-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d835-120">-Name</span></span>
<span data-ttu-id="3d835-121">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="3d835-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d835-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d835-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3d835-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3d835-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d835-124">-Confirm</span></span>
<span data-ttu-id="3d835-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d835-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d835-126">-WhatIf</span></span>
<span data-ttu-id="3d835-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d835-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d835-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d835-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d835-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d835-129">CommonParameters</span></span>
<span data-ttu-id="3d835-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d835-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d835-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d835-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d835-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d835-132">INPUTS</span></span>

### <span data-ttu-id="3d835-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3d835-133">System.String</span></span>

## <span data-ttu-id="3d835-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d835-134">OUTPUTS</span></span>

### <span data-ttu-id="3d835-135">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d835-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="3d835-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d835-136">NOTES</span></span>

## <span data-ttu-id="3d835-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d835-137">RELATED LINKS</span></span>
