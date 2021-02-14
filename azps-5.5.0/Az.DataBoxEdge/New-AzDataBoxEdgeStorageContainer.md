---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115867"
---
# <span data-ttu-id="c42cd-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c42cd-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="c42cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c42cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c42cd-103">Cria um novo contêiner de armazenamento na conta de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c42cd-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="c42cd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c42cd-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c42cd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c42cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c42cd-106">O cmdlet **New-AzDataBoxEdgeStorageContainer** cria um novo contêiner de armazenamento na conta de Armazenamento de Borda em um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="c42cd-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="c42cd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c42cd-107">EXAMPLES</span></span>

### <span data-ttu-id="c42cd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c42cd-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="c42cd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c42cd-109">PARAMETERS</span></span>

### <span data-ttu-id="c42cd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c42cd-110">-AsJob</span></span>
<span data-ttu-id="c42cd-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c42cd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c42cd-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="c42cd-112">-DataFormat</span></span>
<span data-ttu-id="c42cd-113">Definir Formato de Dados, por ex: PageB ltd, BlobBlab</span><span class="sxs-lookup"><span data-stu-id="c42cd-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="c42cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42cd-114">-DefaultProfile</span></span>
<span data-ttu-id="c42cd-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c42cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42cd-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c42cd-116">-DeviceName</span></span>
<span data-ttu-id="c42cd-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c42cd-117">Device Name</span></span>

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

### <span data-ttu-id="c42cd-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c42cd-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="c42cd-119">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="c42cd-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="c42cd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c42cd-120">-Name</span></span>
<span data-ttu-id="c42cd-121">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="c42cd-121">Resource Name</span></span>

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

### <span data-ttu-id="c42cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="c42cd-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c42cd-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c42cd-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c42cd-124">-Confirm</span></span>
<span data-ttu-id="c42cd-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c42cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c42cd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42cd-126">-WhatIf</span></span>
<span data-ttu-id="c42cd-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c42cd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c42cd-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c42cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c42cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42cd-129">CommonParameters</span></span>
<span data-ttu-id="c42cd-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42cd-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c42cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42cd-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="c42cd-132">INPUTS</span></span>

### <span data-ttu-id="c42cd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c42cd-133">System.String</span></span>

## <span data-ttu-id="c42cd-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="c42cd-134">OUTPUTS</span></span>

### <span data-ttu-id="c42cd-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c42cd-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="c42cd-136">Notas</span><span class="sxs-lookup"><span data-stu-id="c42cd-136">NOTES</span></span>

## <span data-ttu-id="c42cd-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c42cd-137">RELATED LINKS</span></span>
