---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115170"
---
# <span data-ttu-id="0b6bf-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b6bf-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="0b6bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6bf-103">Obtém as contas de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="0b6bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b6bf-104">SYNTAX</span></span>

### <span data-ttu-id="0b6bf-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b6bf-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b6bf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b6bf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b6bf-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b6bf-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b6bf-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b6bf-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0b6bf-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b6bf-109">DESCRIPTION</span></span>
<span data-ttu-id="0b6bf-110">O cmdlet **Get-AzStackEdgeStorageAccount** Obtém as contas de armazenamento de borda disponíveis em um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="0b6bf-111">Você pode especificar o nome como um parâmetro no cmdlet para obter as informações de uma conta de armazenamento de borda específica.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="0b6bf-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b6bf-112">EXAMPLES</span></span>

### <span data-ttu-id="0b6bf-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0b6bf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="0b6bf-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0b6bf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="0b6bf-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0b6bf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="0b6bf-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0b6bf-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="0b6bf-117">OS</span><span class="sxs-lookup"><span data-stu-id="0b6bf-117">PARAMETERS</span></span>

### <span data-ttu-id="0b6bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6bf-118">-DefaultProfile</span></span>
<span data-ttu-id="0b6bf-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b6bf-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0b6bf-120">-DeviceName</span></span>
<span data-ttu-id="0b6bf-121">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b6bf-121">Device Name</span></span>

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

### <span data-ttu-id="0b6bf-122">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="0b6bf-122">-DeviceObject</span></span>
<span data-ttu-id="0b6bf-123">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="0b6bf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b6bf-124">-Name</span></span>
<span data-ttu-id="0b6bf-125">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="0b6bf-125">Resource Name</span></span>

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

### <span data-ttu-id="0b6bf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b6bf-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b6bf-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0b6bf-127">Resource Group Name</span></span>

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

### <span data-ttu-id="0b6bf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b6bf-128">-ResourceId</span></span>
<span data-ttu-id="0b6bf-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="0b6bf-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="0b6bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6bf-130">CommonParameters</span></span>
<span data-ttu-id="0b6bf-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6bf-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b6bf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6bf-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b6bf-133">INPUTS</span></span>

### <span data-ttu-id="0b6bf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0b6bf-134">System.String</span></span>

### <span data-ttu-id="0b6bf-135">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0b6bf-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="0b6bf-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b6bf-136">OUTPUTS</span></span>

### <span data-ttu-id="0b6bf-137">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b6bf-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="0b6bf-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b6bf-138">NOTES</span></span>

## <span data-ttu-id="0b6bf-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b6bf-139">RELATED LINKS</span></span>
