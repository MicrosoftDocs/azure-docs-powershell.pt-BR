---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263565"
---
# <span data-ttu-id="8959b-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8959b-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="8959b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8959b-102">SYNOPSIS</span></span>
<span data-ttu-id="8959b-103">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="8959b-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="8959b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8959b-104">SYNTAX</span></span>

### <span data-ttu-id="8959b-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8959b-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8959b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8959b-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8959b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8959b-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8959b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8959b-108">DESCRIPTION</span></span>
<span data-ttu-id="8959b-109">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="8959b-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="8959b-110">Um grupo de sincronização só poderá ser removido quando todos os pontos de extremidade contidos forem excluídos primeiro.</span><span class="sxs-lookup"><span data-stu-id="8959b-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="8959b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8959b-111">EXAMPLES</span></span>

### <span data-ttu-id="8959b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8959b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="8959b-113">Esse comando irá remover o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8959b-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="8959b-114">OS</span><span class="sxs-lookup"><span data-stu-id="8959b-114">PARAMETERS</span></span>

### <span data-ttu-id="8959b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8959b-115">-AsJob</span></span>
<span data-ttu-id="8959b-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8959b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8959b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8959b-117">-DefaultProfile</span></span>
<span data-ttu-id="8959b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8959b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8959b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8959b-119">-Force</span></span>
<span data-ttu-id="8959b-120">Supply-Force para ignorar a confirmação desse comando.</span><span class="sxs-lookup"><span data-stu-id="8959b-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8959b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8959b-121">-InputObject</span></span>
<span data-ttu-id="8959b-122">Objeto de entrada do objeto de sincronização</span><span class="sxs-lookup"><span data-stu-id="8959b-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8959b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8959b-123">-Name</span></span>
<span data-ttu-id="8959b-124">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="8959b-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8959b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8959b-125">-PassThru</span></span>
<span data-ttu-id="8959b-126">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="8959b-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="8959b-127">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8959b-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="8959b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8959b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8959b-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8959b-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8959b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8959b-130">-ResourceId</span></span>
<span data-ttu-id="8959b-131">ID do recurso do pool de sincronização</span><span class="sxs-lookup"><span data-stu-id="8959b-131">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8959b-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="8959b-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="8959b-133">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="8959b-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8959b-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8959b-134">-Confirm</span></span>
<span data-ttu-id="8959b-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8959b-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8959b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8959b-136">-WhatIf</span></span>
<span data-ttu-id="8959b-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8959b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8959b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8959b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8959b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8959b-139">CommonParameters</span></span>
<span data-ttu-id="8959b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8959b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8959b-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8959b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8959b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8959b-142">INPUTS</span></span>

### <span data-ttu-id="8959b-143">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8959b-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="8959b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8959b-144">System.String</span></span>

### <span data-ttu-id="8959b-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8959b-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8959b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8959b-146">OUTPUTS</span></span>

### <span data-ttu-id="8959b-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="8959b-147">System.Object</span></span>
## <span data-ttu-id="8959b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8959b-148">NOTES</span></span>

## <span data-ttu-id="8959b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8959b-149">RELATED LINKS</span></span>
