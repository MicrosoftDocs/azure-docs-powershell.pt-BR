---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 3d44c9def7dd56fa0d3fa58fd417a738c5db051b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600778"
---
# <span data-ttu-id="12c56-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="12c56-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="12c56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12c56-102">SYNOPSIS</span></span>
<span data-ttu-id="12c56-103">Obtém detalhes de um volume do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="12c56-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="12c56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12c56-104">SYNTAX</span></span>

### <span data-ttu-id="12c56-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="12c56-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12c56-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12c56-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12c56-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12c56-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12c56-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12c56-108">DESCRIPTION</span></span>
<span data-ttu-id="12c56-109">O cmdlet **Get-AzNetAppFilesVolume** Obtém detalhes de um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="12c56-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="12c56-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12c56-110">EXAMPLES</span></span>

### <span data-ttu-id="12c56-111">Exemplo 1: obter um volume do ANF</span><span class="sxs-lookup"><span data-stu-id="12c56-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="12c56-112">Esse comando obtém o volume denominado MyAnfVolume do pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="12c56-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="12c56-113">OS</span><span class="sxs-lookup"><span data-stu-id="12c56-113">PARAMETERS</span></span>

### <span data-ttu-id="12c56-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12c56-114">-AccountName</span></span>
<span data-ttu-id="12c56-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="12c56-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="12c56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c56-116">-DefaultProfile</span></span>
<span data-ttu-id="12c56-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12c56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12c56-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="12c56-118">-Name</span></span>
<span data-ttu-id="12c56-119">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="12c56-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c56-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="12c56-120">-PoolName</span></span>
<span data-ttu-id="12c56-121">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="12c56-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="12c56-122">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="12c56-122">-PoolObject</span></span>
<span data-ttu-id="12c56-123">O objeto de pool que contém o volume a ser retornado</span><span class="sxs-lookup"><span data-stu-id="12c56-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12c56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12c56-124">-ResourceGroupName</span></span>
<span data-ttu-id="12c56-125">O grupo de recursos do volume ANF</span><span class="sxs-lookup"><span data-stu-id="12c56-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="12c56-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12c56-126">-ResourceId</span></span>
<span data-ttu-id="12c56-127">A ID do recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="12c56-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="12c56-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c56-128">CommonParameters</span></span>
<span data-ttu-id="12c56-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c56-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="12c56-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c56-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c56-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12c56-131">INPUTS</span></span>

### <span data-ttu-id="12c56-132">System. String</span><span class="sxs-lookup"><span data-stu-id="12c56-132">System.String</span></span>

### <span data-ttu-id="12c56-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="12c56-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="12c56-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12c56-134">OUTPUTS</span></span>

### <span data-ttu-id="12c56-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="12c56-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="12c56-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12c56-136">NOTES</span></span>

## <span data-ttu-id="12c56-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12c56-137">RELATED LINKS</span></span>
