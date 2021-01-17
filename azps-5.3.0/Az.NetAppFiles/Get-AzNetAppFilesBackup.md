---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427071"
---
# <span data-ttu-id="c5595-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="c5595-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="c5595-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5595-102">SYNOPSIS</span></span>
<span data-ttu-id="c5595-103">Obtém detalhes de um backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="c5595-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="c5595-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5595-104">SYNTAX</span></span>

### <span data-ttu-id="c5595-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5595-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5595-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5595-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5595-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5595-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5595-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5595-108">DESCRIPTION</span></span>
<span data-ttu-id="c5595-109">O cmdlet **Get-AzNetAppFilesBackup** Obtém detalhes de um backup do ANF.</span><span class="sxs-lookup"><span data-stu-id="c5595-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="c5595-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5595-110">EXAMPLES</span></span>

### <span data-ttu-id="c5595-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5595-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="c5595-112">Esse comando obtém o backcup chamado "MyAnfAccount" do volume chamado "myvolume".</span><span class="sxs-lookup"><span data-stu-id="c5595-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="c5595-113">OS</span><span class="sxs-lookup"><span data-stu-id="c5595-113">PARAMETERS</span></span>

### <span data-ttu-id="c5595-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5595-114">-AccountName</span></span>
<span data-ttu-id="c5595-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="c5595-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="c5595-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5595-116">-DefaultProfile</span></span>
<span data-ttu-id="c5595-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5595-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5595-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5595-118">-Name</span></span>
<span data-ttu-id="c5595-119">O nome do backup do ANF</span><span class="sxs-lookup"><span data-stu-id="c5595-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5595-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c5595-120">-PoolName</span></span>
<span data-ttu-id="c5595-121">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="c5595-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c5595-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5595-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5595-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="c5595-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c5595-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5595-124">-ResourceId</span></span>
<span data-ttu-id="c5595-125">A ID do recurso do backup do ANF</span><span class="sxs-lookup"><span data-stu-id="c5595-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="c5595-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="c5595-126">-VolumeName</span></span>
<span data-ttu-id="c5595-127">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="c5595-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5595-128">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="c5595-128">-VolumeObject</span></span>
<span data-ttu-id="c5595-129">O objeto de volume que contém o backup a ser retornado</span><span class="sxs-lookup"><span data-stu-id="c5595-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="c5595-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5595-130">CommonParameters</span></span>
<span data-ttu-id="c5595-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5595-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5595-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5595-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5595-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5595-133">INPUTS</span></span>

### <span data-ttu-id="c5595-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c5595-134">System.String</span></span>

### <span data-ttu-id="c5595-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c5595-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c5595-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5595-136">OUTPUTS</span></span>

### <span data-ttu-id="c5595-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="c5595-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="c5595-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5595-138">NOTES</span></span>

## <span data-ttu-id="c5595-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5595-139">RELATED LINKS</span></span>
