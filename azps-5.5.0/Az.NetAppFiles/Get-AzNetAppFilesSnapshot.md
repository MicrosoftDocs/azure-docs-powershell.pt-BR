---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118404"
---
# <span data-ttu-id="70dec-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="70dec-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="70dec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70dec-102">SYNOPSIS</span></span>
<span data-ttu-id="70dec-103">Obtém detalhes de um instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="70dec-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="70dec-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70dec-104">SYNTAX</span></span>

### <span data-ttu-id="70dec-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70dec-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70dec-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70dec-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70dec-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70dec-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70dec-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="70dec-108">DESCRIPTION</span></span>
<span data-ttu-id="70dec-109">O cmdlet **Get-AzNetAppFilesSnapshot obtém** detalhes de um instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="70dec-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="70dec-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70dec-110">EXAMPLES</span></span>

### <span data-ttu-id="70dec-111">Exemplo 1: Obter um instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-111">Example 1: Get an ANF snapshot</span></span>
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
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="70dec-112">Esse comando obtém o instantâneo chamado MyAnfSnapshot do volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="70dec-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="70dec-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70dec-113">PARAMETERS</span></span>

### <span data-ttu-id="70dec-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="70dec-114">-AccountName</span></span>
<span data-ttu-id="70dec-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70dec-116">-DefaultProfile</span></span>
<span data-ttu-id="70dec-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70dec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70dec-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="70dec-118">-Name</span></span>
<span data-ttu-id="70dec-119">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="70dec-120">-PoolName</span></span>
<span data-ttu-id="70dec-121">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70dec-122">-ResourceGroupName</span></span>
<span data-ttu-id="70dec-123">O grupo de recursos do volume de ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-123">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70dec-124">-ResourceId</span></span>
<span data-ttu-id="70dec-125">A ID do recurso do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-126">-Nomedo Volume</span><span class="sxs-lookup"><span data-stu-id="70dec-126">-VolumeName</span></span>
<span data-ttu-id="70dec-127">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="70dec-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="70dec-128">-VolumeObject</span></span>
<span data-ttu-id="70dec-129">O objeto de volume que contém o instantâneo a ser retornado</span><span class="sxs-lookup"><span data-stu-id="70dec-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70dec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70dec-130">CommonParameters</span></span>
<span data-ttu-id="70dec-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70dec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70dec-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70dec-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70dec-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="70dec-133">INPUTS</span></span>

### <span data-ttu-id="70dec-134">System.String</span><span class="sxs-lookup"><span data-stu-id="70dec-134">System.String</span></span>

### <span data-ttu-id="70dec-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="70dec-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="70dec-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="70dec-136">OUTPUTS</span></span>

### <span data-ttu-id="70dec-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="70dec-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="70dec-138">Notas</span><span class="sxs-lookup"><span data-stu-id="70dec-138">NOTES</span></span>

## <span data-ttu-id="70dec-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70dec-139">RELATED LINKS</span></span>
