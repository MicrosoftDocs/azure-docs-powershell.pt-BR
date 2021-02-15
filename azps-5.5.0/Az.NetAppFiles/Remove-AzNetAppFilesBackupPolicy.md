---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117493"
---
# <span data-ttu-id="0df18-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0df18-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="0df18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0df18-102">SYNOPSIS</span></span>
<span data-ttu-id="0df18-103">Exclui uma política de backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="0df18-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="0df18-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0df18-104">SYNTAX</span></span>

### <span data-ttu-id="0df18-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0df18-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df18-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df18-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df18-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0df18-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0df18-109">DESCRIPTION</span></span>
<span data-ttu-id="0df18-110">O cmdlet **Remove-AzNetAppFilesBackupPolicy** exclui uma política de backup ANF.</span><span class="sxs-lookup"><span data-stu-id="0df18-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="0df18-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0df18-111">EXAMPLES</span></span>

### <span data-ttu-id="0df18-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0df18-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="0df18-113">Esse comando exclui a nova política de backup da ANF com o nome "MyBackupPolicy" da conta "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="0df18-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="0df18-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0df18-114">PARAMETERS</span></span>

### <span data-ttu-id="0df18-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="0df18-115">-AccountName</span></span>
<span data-ttu-id="0df18-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="0df18-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="0df18-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0df18-117">-AccountObject</span></span>
<span data-ttu-id="0df18-118">O objeto Conta que contém a Política de Backup a ser removido</span><span class="sxs-lookup"><span data-stu-id="0df18-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="0df18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df18-119">-DefaultProfile</span></span>
<span data-ttu-id="0df18-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0df18-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0df18-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0df18-121">-InputObject</span></span>
<span data-ttu-id="0df18-122">O objeto BackupPolicy a ser removido</span><span class="sxs-lookup"><span data-stu-id="0df18-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="0df18-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0df18-123">-Name</span></span>
<span data-ttu-id="0df18-124">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="0df18-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="0df18-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0df18-125">-PassThru</span></span>
<span data-ttu-id="0df18-126">Retornar se a política de backup especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="0df18-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="0df18-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df18-127">-ResourceGroupName</span></span>
<span data-ttu-id="0df18-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="0df18-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0df18-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0df18-129">-ResourceId</span></span>
<span data-ttu-id="0df18-130">A ID do recurso da Política de Backup da ANF</span><span class="sxs-lookup"><span data-stu-id="0df18-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="0df18-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0df18-131">-Confirm</span></span>
<span data-ttu-id="0df18-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0df18-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0df18-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0df18-133">-WhatIf</span></span>
<span data-ttu-id="0df18-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0df18-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0df18-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0df18-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0df18-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df18-136">CommonParameters</span></span>
<span data-ttu-id="0df18-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df18-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df18-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0df18-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df18-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="0df18-139">INPUTS</span></span>

### <span data-ttu-id="0df18-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0df18-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="0df18-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0df18-141">System.String</span></span>

### <span data-ttu-id="0df18-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0df18-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="0df18-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="0df18-143">OUTPUTS</span></span>

### <span data-ttu-id="0df18-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0df18-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="0df18-145">Notas</span><span class="sxs-lookup"><span data-stu-id="0df18-145">NOTES</span></span>

## <span data-ttu-id="0df18-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0df18-146">RELATED LINKS</span></span>
