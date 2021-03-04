---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: a0fe5dd999d4e5bf8f03d4567e2ba605d42f9cd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892016"
---
# <span data-ttu-id="1df18-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1df18-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1df18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1df18-102">SYNOPSIS</span></span>
<span data-ttu-id="1df18-103">Cria um novo contêiner de armazenamento na conta de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1df18-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="1df18-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1df18-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df18-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1df18-105">DESCRIPTION</span></span>
<span data-ttu-id="1df18-106">O cmdlet **New-AzStackEdgeStorageContainer** cria um novo contêiner de armazenamento na conta de Armazenamento de Borda em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="1df18-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="1df18-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1df18-107">EXAMPLES</span></span>

### <span data-ttu-id="1df18-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1df18-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="1df18-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1df18-109">PARAMETERS</span></span>

### <span data-ttu-id="1df18-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1df18-110">-AsJob</span></span>
<span data-ttu-id="1df18-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1df18-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1df18-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="1df18-112">-DataFormat</span></span>
<span data-ttu-id="1df18-113">Definir Formato de Dados ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="1df18-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="1df18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df18-114">-DefaultProfile</span></span>
<span data-ttu-id="1df18-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1df18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1df18-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1df18-116">-DeviceName</span></span>
<span data-ttu-id="1df18-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="1df18-117">Device Name</span></span>

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

### <span data-ttu-id="1df18-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1df18-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="1df18-119">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="1df18-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="1df18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1df18-120">-Name</span></span>
<span data-ttu-id="1df18-121">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="1df18-121">Resource Name</span></span>

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

### <span data-ttu-id="1df18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df18-122">-ResourceGroupName</span></span>
<span data-ttu-id="1df18-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1df18-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1df18-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1df18-124">-Confirm</span></span>
<span data-ttu-id="1df18-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1df18-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1df18-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df18-126">-WhatIf</span></span>
<span data-ttu-id="1df18-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1df18-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1df18-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1df18-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1df18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df18-129">CommonParameters</span></span>
<span data-ttu-id="1df18-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df18-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1df18-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df18-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1df18-132">INPUTS</span></span>

### <span data-ttu-id="1df18-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1df18-133">System.String</span></span>

## <span data-ttu-id="1df18-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1df18-134">OUTPUTS</span></span>

### <span data-ttu-id="1df18-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1df18-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1df18-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="1df18-136">NOTES</span></span>

## <span data-ttu-id="1df18-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1df18-137">RELATED LINKS</span></span>
