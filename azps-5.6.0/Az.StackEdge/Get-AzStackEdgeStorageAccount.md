---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: a5844e4d03be96d4835a7bf83b2128958cee0b5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890696"
---
# <span data-ttu-id="86751-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86751-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="86751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86751-102">SYNOPSIS</span></span>
<span data-ttu-id="86751-103">Obtém as contas de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86751-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="86751-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="86751-104">SYNTAX</span></span>

### <span data-ttu-id="86751-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="86751-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86751-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86751-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86751-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86751-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86751-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86751-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="86751-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="86751-109">DESCRIPTION</span></span>
<span data-ttu-id="86751-110">O cmdlet **Get-AzStackEdgeStorageAccount** obtém as contas de Armazenamento de Borda disponíveis em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="86751-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="86751-111">Você pode especificar o Nome como um parâmetro no cmdlet para obter as informações de uma conta de Armazenamento de Borda específica.</span><span class="sxs-lookup"><span data-stu-id="86751-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="86751-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86751-112">EXAMPLES</span></span>

### <span data-ttu-id="86751-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="86751-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="86751-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="86751-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="86751-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="86751-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="86751-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="86751-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="86751-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="86751-117">PARAMETERS</span></span>

### <span data-ttu-id="86751-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86751-118">-DefaultProfile</span></span>
<span data-ttu-id="86751-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86751-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86751-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="86751-120">-DeviceName</span></span>
<span data-ttu-id="86751-121">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="86751-121">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86751-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="86751-122">-DeviceObject</span></span>
<span data-ttu-id="86751-123">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="86751-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86751-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86751-124">-Name</span></span>
<span data-ttu-id="86751-125">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="86751-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86751-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86751-126">-ResourceGroupName</span></span>
<span data-ttu-id="86751-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="86751-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86751-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86751-128">-ResourceId</span></span>
<span data-ttu-id="86751-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="86751-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86751-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86751-130">CommonParameters</span></span>
<span data-ttu-id="86751-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86751-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86751-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86751-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86751-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86751-133">INPUTS</span></span>

### <span data-ttu-id="86751-134">System.String</span><span class="sxs-lookup"><span data-stu-id="86751-134">System.String</span></span>

### <span data-ttu-id="86751-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="86751-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="86751-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="86751-136">OUTPUTS</span></span>

### <span data-ttu-id="86751-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86751-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="86751-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="86751-138">NOTES</span></span>

## <span data-ttu-id="86751-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86751-139">RELATED LINKS</span></span>
