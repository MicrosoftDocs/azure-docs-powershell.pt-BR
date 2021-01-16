---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262601"
---
# <span data-ttu-id="d26af-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d26af-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d26af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d26af-102">SYNOPSIS</span></span>
<span data-ttu-id="d26af-103">Exclui uma política de backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="d26af-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="d26af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d26af-104">SYNTAX</span></span>

### <span data-ttu-id="d26af-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d26af-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d26af-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d26af-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d26af-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d26af-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d26af-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d26af-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d26af-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d26af-109">DESCRIPTION</span></span>
<span data-ttu-id="d26af-110">O cmdlet **Remove-AzNetAppFilesBackupPolicy** exclui uma política de backup do ANF.</span><span class="sxs-lookup"><span data-stu-id="d26af-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="d26af-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d26af-111">EXAMPLES</span></span>

### <span data-ttu-id="d26af-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d26af-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="d26af-113">Esse comando exclui a nova política de backup do ANF com o nome "MyBackupPolicy" para a conta "myaccount".</span><span class="sxs-lookup"><span data-stu-id="d26af-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="d26af-114">OS</span><span class="sxs-lookup"><span data-stu-id="d26af-114">PARAMETERS</span></span>

### <span data-ttu-id="d26af-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d26af-115">-AccountName</span></span>
<span data-ttu-id="d26af-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="d26af-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d26af-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="d26af-117">-AccountObject</span></span>
<span data-ttu-id="d26af-118">O objeto de conta que contém a política de backup a ser removida</span><span class="sxs-lookup"><span data-stu-id="d26af-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="d26af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26af-119">-DefaultProfile</span></span>
<span data-ttu-id="d26af-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d26af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d26af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d26af-121">-InputObject</span></span>
<span data-ttu-id="d26af-122">O objeto BackupPolicy para remover</span><span class="sxs-lookup"><span data-stu-id="d26af-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d26af-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d26af-123">-Name</span></span>
<span data-ttu-id="d26af-124">O nome da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="d26af-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26af-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d26af-125">-PassThru</span></span>
<span data-ttu-id="d26af-126">Retornar se a política de backup especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="d26af-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="d26af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d26af-127">-ResourceGroupName</span></span>
<span data-ttu-id="d26af-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="d26af-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d26af-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d26af-129">-ResourceId</span></span>
<span data-ttu-id="d26af-130">A ID do recurso da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="d26af-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="d26af-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d26af-131">-Confirm</span></span>
<span data-ttu-id="d26af-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d26af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d26af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d26af-133">-WhatIf</span></span>
<span data-ttu-id="d26af-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d26af-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d26af-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d26af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d26af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26af-136">CommonParameters</span></span>
<span data-ttu-id="d26af-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d26af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26af-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d26af-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26af-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d26af-139">INPUTS</span></span>

### <span data-ttu-id="d26af-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d26af-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="d26af-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d26af-141">System.String</span></span>

### <span data-ttu-id="d26af-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d26af-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d26af-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d26af-143">OUTPUTS</span></span>

### <span data-ttu-id="d26af-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d26af-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d26af-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d26af-145">NOTES</span></span>

## <span data-ttu-id="d26af-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d26af-146">RELATED LINKS</span></span>
