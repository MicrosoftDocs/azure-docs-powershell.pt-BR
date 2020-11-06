---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600770"
---
# <span data-ttu-id="1b8d8-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1b8d8-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="1b8d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8d8-103">Cria um novo volume de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="1b8d8-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="1b8d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b8d8-104">SYNTAX</span></span>

### <span data-ttu-id="1b8d8-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b8d8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b8d8-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b8d8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="1b8d8-108">O cmdlet **New-AzNetAppFilesVolume** cria um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="1b8d8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b8d8-109">EXAMPLES</span></span>

### <span data-ttu-id="1b8d8-110">Exemplo 1: criar um volume do ANF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="1b8d8-111">Esse comando cria o novo volume ANF "MyAnfVolume" no pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="1b8d8-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="1b8d8-112">OS</span><span class="sxs-lookup"><span data-stu-id="1b8d8-112">PARAMETERS</span></span>

### <span data-ttu-id="1b8d8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b8d8-113">-AccountName</span></span>
<span data-ttu-id="1b8d8-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="1b8d8-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="1b8d8-115">-CreationToken</span></span>
<span data-ttu-id="1b8d8-116">Um caminho de arquivo exclusivo para o volume</span><span class="sxs-lookup"><span data-stu-id="1b8d8-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b8d8-117">-DefaultProfile</span></span>
<span data-ttu-id="1b8d8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b8d8-119">-Local</span><span class="sxs-lookup"><span data-stu-id="1b8d8-119">-Location</span></span>
<span data-ttu-id="1b8d8-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="1b8d8-120">The location of the resource</span></span>

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

### <span data-ttu-id="1b8d8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b8d8-121">-Name</span></span>
<span data-ttu-id="1b8d8-122">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1b8d8-123">-PoolName</span></span>
<span data-ttu-id="1b8d8-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1b8d8-125">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="1b8d8-125">-PoolObject</span></span>
<span data-ttu-id="1b8d8-126">O pool para o novo objeto de volume</span><span class="sxs-lookup"><span data-stu-id="1b8d8-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="1b8d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b8d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b8d8-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1b8d8-129">-Nível de</span><span class="sxs-lookup"><span data-stu-id="1b8d8-129">-ServiceLevel</span></span>
<span data-ttu-id="1b8d8-130">O nível de serviço do volume ANF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-130">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-131">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="1b8d8-131">-SubnetId</span></span>
<span data-ttu-id="1b8d8-132">O URI do recurso do Azure para uma sub-rede delegada</span><span class="sxs-lookup"><span data-stu-id="1b8d8-132">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="1b8d8-133">-Tag</span></span>
<span data-ttu-id="1b8d8-134">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="1b8d8-134">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="1b8d8-135">-UsageThreshold</span></span>
<span data-ttu-id="1b8d8-136">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="1b8d8-136">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b8d8-137">-Confirm</span></span>
<span data-ttu-id="1b8d8-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b8d8-139">-WhatIf</span></span>
<span data-ttu-id="1b8d8-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b8d8-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8d8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8d8-142">CommonParameters</span></span>
<span data-ttu-id="1b8d8-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1b8d8-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b8d8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8d8-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b8d8-145">INPUTS</span></span>

### <span data-ttu-id="1b8d8-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1b8d8-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="1b8d8-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b8d8-147">OUTPUTS</span></span>

### <span data-ttu-id="1b8d8-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1b8d8-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1b8d8-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b8d8-149">NOTES</span></span>

## <span data-ttu-id="1b8d8-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b8d8-150">RELATED LINKS</span></span>
