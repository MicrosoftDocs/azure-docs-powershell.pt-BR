---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943175"
---
# <span data-ttu-id="5e297-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5e297-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="5e297-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e297-102">SYNOPSIS</span></span>
<span data-ttu-id="5e297-103">Esse comando excluirá o serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="5e297-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="5e297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e297-104">SYNTAX</span></span>

### <span data-ttu-id="5e297-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e297-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e297-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e297-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e297-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e297-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e297-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e297-108">DESCRIPTION</span></span>
<span data-ttu-id="5e297-109">Esse comando excluirá o serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="5e297-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="5e297-110">Um serviço de sincronização de armazenamento só pode ser removido quando todos os grupos de sincronização e servidores registrados contidos são excluídos primeiro.</span><span class="sxs-lookup"><span data-stu-id="5e297-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="5e297-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e297-111">EXAMPLES</span></span>

### <span data-ttu-id="5e297-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e297-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="5e297-113">Esse comando irá remover o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5e297-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="5e297-114">OS</span><span class="sxs-lookup"><span data-stu-id="5e297-114">PARAMETERS</span></span>

### <span data-ttu-id="5e297-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e297-115">-AsJob</span></span>
<span data-ttu-id="5e297-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5e297-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e297-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e297-117">-DefaultProfile</span></span>
<span data-ttu-id="5e297-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e297-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e297-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5e297-119">-Force</span></span>
<span data-ttu-id="5e297-120">Supply-Force para ignorar a confirmação desse comando.</span><span class="sxs-lookup"><span data-stu-id="5e297-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="5e297-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e297-121">-InputObject</span></span>
<span data-ttu-id="5e297-122">Objeto de entrada StorageSyncService, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e297-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e297-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e297-123">-Name</span></span>
<span data-ttu-id="5e297-124">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5e297-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e297-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e297-125">-PassThru</span></span>
<span data-ttu-id="5e297-126">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="5e297-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="5e297-127">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5e297-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="5e297-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e297-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e297-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e297-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e297-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e297-130">-ResourceId</span></span>
<span data-ttu-id="5e297-131">ID do recurso StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5e297-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="5e297-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e297-132">-Confirm</span></span>
<span data-ttu-id="5e297-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e297-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e297-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e297-134">-WhatIf</span></span>
<span data-ttu-id="5e297-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e297-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e297-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e297-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e297-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e297-137">CommonParameters</span></span>
<span data-ttu-id="5e297-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e297-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e297-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e297-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e297-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e297-140">INPUTS</span></span>

### <span data-ttu-id="5e297-141">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5e297-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="5e297-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5e297-142">System.String</span></span>

### <span data-ttu-id="5e297-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5e297-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5e297-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e297-144">OUTPUTS</span></span>

### <span data-ttu-id="5e297-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="5e297-145">System.Object</span></span>
## <span data-ttu-id="5e297-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e297-146">NOTES</span></span>

## <span data-ttu-id="5e297-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e297-147">RELATED LINKS</span></span>
