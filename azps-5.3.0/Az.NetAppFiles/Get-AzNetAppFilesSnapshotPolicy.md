---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427065"
---
# <span data-ttu-id="ef35c-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ef35c-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ef35c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef35c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef35c-103">Obtém detalhes de uma política de instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="ef35c-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="ef35c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef35c-104">SYNTAX</span></span>

### <span data-ttu-id="ef35c-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef35c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef35c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef35c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef35c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef35c-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef35c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef35c-108">DESCRIPTION</span></span>
<span data-ttu-id="ef35c-109">O cmdlet **Get-AzNetAppFilesSnapshotPolicy** Obtém detalhes de uma política de instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="ef35c-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="ef35c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef35c-110">EXAMPLES</span></span>

### <span data-ttu-id="ef35c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef35c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="ef35c-112">Esse comando obtém a política de backup chamada "MyBackupPolicy" para a conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="ef35c-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="ef35c-113">OS</span><span class="sxs-lookup"><span data-stu-id="ef35c-113">PARAMETERS</span></span>

### <span data-ttu-id="ef35c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef35c-114">-AccountName</span></span>
<span data-ttu-id="ef35c-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="ef35c-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ef35c-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="ef35c-116">-AccountObject</span></span>
<span data-ttu-id="ef35c-117">A conta para o novo objeto de política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="ef35c-117">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef35c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef35c-118">-DefaultProfile</span></span>
<span data-ttu-id="ef35c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef35c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef35c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef35c-120">-Name</span></span>
<span data-ttu-id="ef35c-121">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="ef35c-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef35c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef35c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef35c-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="ef35c-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ef35c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef35c-124">-ResourceId</span></span>
<span data-ttu-id="ef35c-125">A ID do recurso da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="ef35c-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="ef35c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef35c-126">-Confirm</span></span>
<span data-ttu-id="ef35c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef35c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef35c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef35c-128">-WhatIf</span></span>
<span data-ttu-id="ef35c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef35c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef35c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef35c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef35c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef35c-131">CommonParameters</span></span>
<span data-ttu-id="ef35c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef35c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef35c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef35c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef35c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef35c-134">INPUTS</span></span>

### <span data-ttu-id="ef35c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ef35c-135">System.String</span></span>

### <span data-ttu-id="ef35c-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ef35c-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ef35c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef35c-137">OUTPUTS</span></span>

### <span data-ttu-id="ef35c-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ef35c-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ef35c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef35c-139">NOTES</span></span>

## <span data-ttu-id="ef35c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef35c-140">RELATED LINKS</span></span>
