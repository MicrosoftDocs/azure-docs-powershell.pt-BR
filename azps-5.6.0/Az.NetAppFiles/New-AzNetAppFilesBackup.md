---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 6b4527430fa74efa09aa07fd120d0acf8de0edfd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887446"
---
# <span data-ttu-id="a73de-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="a73de-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="a73de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a73de-102">SYNOPSIS</span></span>
<span data-ttu-id="a73de-103">Cria um novo backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="a73de-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="a73de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a73de-104">SYNTAX</span></span>

### <span data-ttu-id="a73de-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a73de-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a73de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a73de-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a73de-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a73de-107">DESCRIPTION</span></span>
<span data-ttu-id="a73de-108">O cmdlet **New-AzNetAppFilesBackup** cria um backup para um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="a73de-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="a73de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a73de-109">EXAMPLES</span></span>

### <span data-ttu-id="a73de-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a73de-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="a73de-111">Este comando cria o novo backup ANF para a conta "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="a73de-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="a73de-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a73de-112">PARAMETERS</span></span>

### <span data-ttu-id="a73de-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a73de-113">-AccountName</span></span>
<span data-ttu-id="a73de-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a73de-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a73de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73de-115">-DefaultProfile</span></span>
<span data-ttu-id="a73de-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a73de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a73de-117">-Label</span><span class="sxs-lookup"><span data-stu-id="a73de-117">-Label</span></span>
<span data-ttu-id="a73de-118">Rótulo para backup</span><span class="sxs-lookup"><span data-stu-id="a73de-118">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73de-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a73de-119">-Location</span></span>
<span data-ttu-id="a73de-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="a73de-120">The location of the resource</span></span>

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

### <span data-ttu-id="a73de-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a73de-121">-Name</span></span>
<span data-ttu-id="a73de-122">O nome do backup da ANF</span><span class="sxs-lookup"><span data-stu-id="a73de-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73de-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a73de-123">-PoolName</span></span>
<span data-ttu-id="a73de-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="a73de-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a73de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73de-125">-ResourceGroupName</span></span>
<span data-ttu-id="a73de-126">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a73de-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a73de-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="a73de-127">-VolumeName</span></span>
<span data-ttu-id="a73de-128">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="a73de-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a73de-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="a73de-129">-VolumeObject</span></span>
<span data-ttu-id="a73de-130">O volume do novo objeto de backup</span><span class="sxs-lookup"><span data-stu-id="a73de-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="a73de-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a73de-131">-Confirm</span></span>
<span data-ttu-id="a73de-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a73de-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a73de-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73de-133">-WhatIf</span></span>
<span data-ttu-id="a73de-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a73de-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73de-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a73de-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a73de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73de-136">CommonParameters</span></span>
<span data-ttu-id="a73de-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73de-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a73de-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73de-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a73de-139">INPUTS</span></span>

### <span data-ttu-id="a73de-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a73de-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a73de-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a73de-141">OUTPUTS</span></span>

### <span data-ttu-id="a73de-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="a73de-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="a73de-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="a73de-143">NOTES</span></span>

## <span data-ttu-id="a73de-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a73de-144">RELATED LINKS</span></span>
