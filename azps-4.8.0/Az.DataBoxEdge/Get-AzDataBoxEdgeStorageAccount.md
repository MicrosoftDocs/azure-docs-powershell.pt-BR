---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112355"
---
# <span data-ttu-id="47908-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47908-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="47908-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47908-102">SYNOPSIS</span></span>
<span data-ttu-id="47908-103">Obtém as contas de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47908-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="47908-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47908-104">SYNTAX</span></span>

### <span data-ttu-id="47908-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="47908-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47908-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47908-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47908-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47908-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47908-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47908-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="47908-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47908-109">DESCRIPTION</span></span>
<span data-ttu-id="47908-110">O cmdlet **Get-AzDataBoxEdgeStorageAccount** Obtém as contas de armazenamento de borda disponíveis em um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="47908-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="47908-111">Você pode especificar o nome como um parâmetro no cmdlet para obter as informações de uma conta de armazenamento de borda específica.</span><span class="sxs-lookup"><span data-stu-id="47908-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="47908-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47908-112">EXAMPLES</span></span>

### <span data-ttu-id="47908-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47908-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="47908-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47908-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="47908-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="47908-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="47908-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="47908-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="47908-117">OS</span><span class="sxs-lookup"><span data-stu-id="47908-117">PARAMETERS</span></span>

### <span data-ttu-id="47908-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47908-118">-DefaultProfile</span></span>
<span data-ttu-id="47908-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47908-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47908-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="47908-120">-DeviceName</span></span>
<span data-ttu-id="47908-121">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="47908-121">Device Name</span></span>

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

### <span data-ttu-id="47908-122">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="47908-122">-DeviceObject</span></span>
<span data-ttu-id="47908-123">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="47908-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="47908-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="47908-124">-Name</span></span>
<span data-ttu-id="47908-125">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="47908-125">Resource Name</span></span>

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

### <span data-ttu-id="47908-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47908-126">-ResourceGroupName</span></span>
<span data-ttu-id="47908-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="47908-127">Resource Group Name</span></span>

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

### <span data-ttu-id="47908-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47908-128">-ResourceId</span></span>
<span data-ttu-id="47908-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="47908-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="47908-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47908-130">CommonParameters</span></span>
<span data-ttu-id="47908-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47908-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47908-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47908-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47908-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47908-133">INPUTS</span></span>

### <span data-ttu-id="47908-134">System. String</span><span class="sxs-lookup"><span data-stu-id="47908-134">System.String</span></span>

### <span data-ttu-id="47908-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="47908-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="47908-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47908-136">OUTPUTS</span></span>

### <span data-ttu-id="47908-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47908-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="47908-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47908-138">NOTES</span></span>

## <span data-ttu-id="47908-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47908-139">RELATED LINKS</span></span>
