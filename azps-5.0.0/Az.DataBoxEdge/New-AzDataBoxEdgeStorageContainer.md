---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281129"
---
# <span data-ttu-id="1eb2a-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1eb2a-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="1eb2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb2a-103">Cria um novo contêiner de armazenamento na conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="1eb2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eb2a-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb2a-106">O cmdlet **New-AzDataBoxEdgeStorageContainer** cria um novo contêiner de armazenamento na conta de armazenamento de borda em um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="1eb2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eb2a-107">EXAMPLES</span></span>

### <span data-ttu-id="1eb2a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1eb2a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="1eb2a-109">OS</span><span class="sxs-lookup"><span data-stu-id="1eb2a-109">PARAMETERS</span></span>

### <span data-ttu-id="1eb2a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eb2a-110">-AsJob</span></span>
<span data-ttu-id="1eb2a-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1eb2a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1eb2a-112">-Formato DataFormat</span><span class="sxs-lookup"><span data-stu-id="1eb2a-112">-DataFormat</span></span>
<span data-ttu-id="1eb2a-113">Definir formato de dados por exemplo: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="1eb2a-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="1eb2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb2a-114">-DefaultProfile</span></span>
<span data-ttu-id="1eb2a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb2a-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1eb2a-116">-DeviceName</span></span>
<span data-ttu-id="1eb2a-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="1eb2a-117">Device Name</span></span>

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

### <span data-ttu-id="1eb2a-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1eb2a-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="1eb2a-119">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="1eb2a-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="1eb2a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eb2a-120">-Name</span></span>
<span data-ttu-id="1eb2a-121">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="1eb2a-121">Resource Name</span></span>

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

### <span data-ttu-id="1eb2a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb2a-122">-ResourceGroupName</span></span>
<span data-ttu-id="1eb2a-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1eb2a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1eb2a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1eb2a-124">-Confirm</span></span>
<span data-ttu-id="1eb2a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb2a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb2a-126">-WhatIf</span></span>
<span data-ttu-id="1eb2a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1eb2a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb2a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb2a-129">CommonParameters</span></span>
<span data-ttu-id="1eb2a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb2a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb2a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb2a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb2a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eb2a-132">INPUTS</span></span>

### <span data-ttu-id="1eb2a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb2a-133">System.String</span></span>

## <span data-ttu-id="1eb2a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eb2a-134">OUTPUTS</span></span>

### <span data-ttu-id="1eb2a-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1eb2a-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="1eb2a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eb2a-136">NOTES</span></span>

## <span data-ttu-id="1eb2a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eb2a-137">RELATED LINKS</span></span>
