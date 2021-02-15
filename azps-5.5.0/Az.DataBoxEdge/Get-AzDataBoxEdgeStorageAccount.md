---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115444"
---
# <span data-ttu-id="e4977-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4977-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e4977-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4977-102">SYNOPSIS</span></span>
<span data-ttu-id="e4977-103">Obtém as contas de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4977-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="e4977-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4977-104">SYNTAX</span></span>

### <span data-ttu-id="e4977-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4977-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4977-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4977-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4977-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4977-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4977-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4977-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e4977-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4977-109">DESCRIPTION</span></span>
<span data-ttu-id="e4977-110">O cmdlet **Get-AzDataBoxEdgeStorageAccount** obtém as contas de Armazenamento de Borda disponíveis em um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="e4977-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="e4977-111">Você pode especificar o Nome como um parâmetro no cmdlet para obter as informações de uma conta de Armazenamento de Borda específica.</span><span class="sxs-lookup"><span data-stu-id="e4977-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="e4977-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4977-112">EXAMPLES</span></span>

### <span data-ttu-id="e4977-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4977-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="e4977-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4977-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="e4977-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e4977-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="e4977-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e4977-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="e4977-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4977-117">PARAMETERS</span></span>

### <span data-ttu-id="e4977-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4977-118">-DefaultProfile</span></span>
<span data-ttu-id="e4977-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4977-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4977-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e4977-120">-DeviceName</span></span>
<span data-ttu-id="e4977-121">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e4977-121">Device Name</span></span>

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

### <span data-ttu-id="e4977-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e4977-122">-DeviceObject</span></span>
<span data-ttu-id="e4977-123">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="e4977-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4977-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4977-124">-Name</span></span>
<span data-ttu-id="e4977-125">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="e4977-125">Resource Name</span></span>

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

### <span data-ttu-id="e4977-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4977-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4977-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e4977-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e4977-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4977-128">-ResourceId</span></span>
<span data-ttu-id="e4977-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4977-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="e4977-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4977-130">CommonParameters</span></span>
<span data-ttu-id="e4977-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4977-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4977-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4977-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4977-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4977-133">INPUTS</span></span>

### <span data-ttu-id="e4977-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e4977-134">System.String</span></span>

### <span data-ttu-id="e4977-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e4977-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e4977-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4977-136">OUTPUTS</span></span>

### <span data-ttu-id="e4977-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4977-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e4977-138">Notas</span><span class="sxs-lookup"><span data-stu-id="e4977-138">NOTES</span></span>

## <span data-ttu-id="e4977-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4977-139">RELATED LINKS</span></span>
