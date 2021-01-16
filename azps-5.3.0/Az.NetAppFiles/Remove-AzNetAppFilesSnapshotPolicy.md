---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271950"
---
# <span data-ttu-id="f91a4-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f91a4-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f91a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f91a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f91a4-103">Exclui uma política de instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="f91a4-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="f91a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f91a4-104">SYNTAX</span></span>

### <span data-ttu-id="f91a4-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f91a4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f91a4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f91a4-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f91a4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f91a4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f91a4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f91a4-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f91a4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f91a4-109">DESCRIPTION</span></span>
<span data-ttu-id="f91a4-110">O cmdlet **Remove-AzNetAppFilesSnapshotPolicy** exclui uma política de instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="f91a4-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="f91a4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f91a4-111">EXAMPLES</span></span>

### <span data-ttu-id="f91a4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f91a4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="f91a4-113">Esse comando exclui a nova política de backup do ANF com o nome "MyBackupPolicy" para a conta "myaccount".</span><span class="sxs-lookup"><span data-stu-id="f91a4-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="f91a4-114">OS</span><span class="sxs-lookup"><span data-stu-id="f91a4-114">PARAMETERS</span></span>

### <span data-ttu-id="f91a4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f91a4-115">-AccountName</span></span>
<span data-ttu-id="f91a4-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="f91a4-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f91a4-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="f91a4-117">-AccountObject</span></span>
<span data-ttu-id="f91a4-118">A conta para o novo objeto de política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="f91a4-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="f91a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91a4-119">-DefaultProfile</span></span>
<span data-ttu-id="f91a4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f91a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91a4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f91a4-121">-InputObject</span></span>
<span data-ttu-id="f91a4-122">O objeto SnapshotPolicy para remover</span><span class="sxs-lookup"><span data-stu-id="f91a4-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f91a4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f91a4-123">-Name</span></span>
<span data-ttu-id="f91a4-124">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="f91a4-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91a4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f91a4-125">-PassThru</span></span>
<span data-ttu-id="f91a4-126">Retornar se a conta especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="f91a4-126">Return whether the specified account was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="f91a4-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="f91a4-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f91a4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f91a4-129">-ResourceId</span></span>
<span data-ttu-id="f91a4-130">A ID do recurso da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="f91a4-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="f91a4-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f91a4-131">-Confirm</span></span>
<span data-ttu-id="f91a4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f91a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91a4-133">-WhatIf</span></span>
<span data-ttu-id="f91a4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f91a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f91a4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f91a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91a4-136">CommonParameters</span></span>
<span data-ttu-id="f91a4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f91a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91a4-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f91a4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91a4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f91a4-139">INPUTS</span></span>

### <span data-ttu-id="f91a4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f91a4-140">System.String</span></span>

### <span data-ttu-id="f91a4-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f91a4-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f91a4-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f91a4-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f91a4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f91a4-143">OUTPUTS</span></span>

### <span data-ttu-id="f91a4-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f91a4-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f91a4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f91a4-145">NOTES</span></span>

## <span data-ttu-id="f91a4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f91a4-146">RELATED LINKS</span></span>
