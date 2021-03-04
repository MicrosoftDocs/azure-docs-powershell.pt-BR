---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 22f8d81ca68c0136802500876102fa53f8ea7a9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888708"
---
# <span data-ttu-id="56457-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="56457-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="56457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56457-102">SYNOPSIS</span></span>
<span data-ttu-id="56457-103">Cria um novo contêiner de armazenamento na conta de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56457-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="56457-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56457-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56457-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56457-105">DESCRIPTION</span></span>
<span data-ttu-id="56457-106">O cmdlet **New-AzDataBoxEdgeStorageContainer** cria um novo contêiner de armazenamento na conta de Armazenamento de Borda em um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="56457-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="56457-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56457-107">EXAMPLES</span></span>

### <span data-ttu-id="56457-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56457-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="56457-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56457-109">PARAMETERS</span></span>

### <span data-ttu-id="56457-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56457-110">-AsJob</span></span>
<span data-ttu-id="56457-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="56457-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56457-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="56457-112">-DataFormat</span></span>
<span data-ttu-id="56457-113">Definir Formato de Dados ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="56457-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="56457-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56457-114">-DefaultProfile</span></span>
<span data-ttu-id="56457-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56457-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56457-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="56457-116">-DeviceName</span></span>
<span data-ttu-id="56457-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="56457-117">Device Name</span></span>

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

### <span data-ttu-id="56457-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="56457-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="56457-119">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="56457-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="56457-120">-Name</span><span class="sxs-lookup"><span data-stu-id="56457-120">-Name</span></span>
<span data-ttu-id="56457-121">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="56457-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56457-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56457-122">-ResourceGroupName</span></span>
<span data-ttu-id="56457-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="56457-123">Resource Group Name</span></span>

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

### <span data-ttu-id="56457-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56457-124">-Confirm</span></span>
<span data-ttu-id="56457-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56457-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56457-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56457-126">-WhatIf</span></span>
<span data-ttu-id="56457-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56457-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56457-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56457-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56457-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56457-129">CommonParameters</span></span>
<span data-ttu-id="56457-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56457-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56457-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56457-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56457-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56457-132">INPUTS</span></span>

### <span data-ttu-id="56457-133">System.String</span><span class="sxs-lookup"><span data-stu-id="56457-133">System.String</span></span>

## <span data-ttu-id="56457-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56457-134">OUTPUTS</span></span>

### <span data-ttu-id="56457-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="56457-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="56457-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="56457-136">NOTES</span></span>

## <span data-ttu-id="56457-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56457-137">RELATED LINKS</span></span>
