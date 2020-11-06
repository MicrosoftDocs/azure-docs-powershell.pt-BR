---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 8f34145a65cde73ea1a5b925064c2b9a1d3f92a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600779"
---
# <span data-ttu-id="d5ebe-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5ebe-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d5ebe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ebe-103">Obtém detalhes de um instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="d5ebe-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="d5ebe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5ebe-104">SYNTAX</span></span>

### <span data-ttu-id="d5ebe-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5ebe-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5ebe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5ebe-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5ebe-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5ebe-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5ebe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5ebe-108">DESCRIPTION</span></span>
<span data-ttu-id="d5ebe-109">O cmdlet **Get-AzNetAppFilesSnapshot** Obtém detalhes de um instantâneo do ANF.</span><span class="sxs-lookup"><span data-stu-id="d5ebe-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="d5ebe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5ebe-110">EXAMPLES</span></span>

### <span data-ttu-id="d5ebe-111">Exemplo 1: obter um instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="d5ebe-112">Esse comando obtém o instantâneo chamado MyAnfSnapshot do volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="d5ebe-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="d5ebe-113">OS</span><span class="sxs-lookup"><span data-stu-id="d5ebe-113">PARAMETERS</span></span>

### <span data-ttu-id="d5ebe-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5ebe-114">-AccountName</span></span>
<span data-ttu-id="d5ebe-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ebe-116">-DefaultProfile</span></span>
<span data-ttu-id="d5ebe-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ebe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5ebe-118">-Name</span></span>
<span data-ttu-id="d5ebe-119">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d5ebe-120">-PoolName</span></span>
<span data-ttu-id="d5ebe-121">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ebe-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5ebe-123">O grupo de recursos do volume ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-123">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5ebe-124">-ResourceId</span></span>
<span data-ttu-id="d5ebe-125">A ID do recurso do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="d5ebe-126">-VolumeName</span></span>
<span data-ttu-id="d5ebe-127">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="d5ebe-127">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-128">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="d5ebe-128">-VolumeObject</span></span>
<span data-ttu-id="d5ebe-129">O objeto volume que contém o instantâneo a ser retornado</span><span class="sxs-lookup"><span data-stu-id="d5ebe-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ebe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ebe-130">CommonParameters</span></span>
<span data-ttu-id="d5ebe-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ebe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d5ebe-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ebe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ebe-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5ebe-133">INPUTS</span></span>

### <span data-ttu-id="d5ebe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5ebe-134">System.String</span></span>

### <span data-ttu-id="d5ebe-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d5ebe-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d5ebe-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5ebe-136">OUTPUTS</span></span>

### <span data-ttu-id="d5ebe-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5ebe-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d5ebe-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5ebe-138">NOTES</span></span>

## <span data-ttu-id="d5ebe-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5ebe-139">RELATED LINKS</span></span>
