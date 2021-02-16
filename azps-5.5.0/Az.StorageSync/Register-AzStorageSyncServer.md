---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118560"
---
# <span data-ttu-id="806e6-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="806e6-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="806e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="806e6-102">SYNOPSIS</span></span>
<span data-ttu-id="806e6-103">Esse comando registra um servidor em um serviço de sincronização de armazenamento que cria uma relação de confiança.</span><span class="sxs-lookup"><span data-stu-id="806e6-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="806e6-104">O PowerShell ou o portal do Azure podem ser usados para configurar a sincronização neste servidor.</span><span class="sxs-lookup"><span data-stu-id="806e6-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="806e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="806e6-105">SYNTAX</span></span>

### <span data-ttu-id="806e6-106">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="806e6-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="806e6-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="806e6-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="806e6-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="806e6-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="806e6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="806e6-109">DESCRIPTION</span></span>
<span data-ttu-id="806e6-110">Esse comando registra um servidor em um serviço de sincronização de armazenamento, o recurso de nível superior para a Sincronização de Arquivos do Azure. Uma relação de confiança entre o servidor e o serviço de sincronização de armazenamento é criada que garante canais de gerenciamento e transferência de dados seguros.</span><span class="sxs-lookup"><span data-stu-id="806e6-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="806e6-111">O PowerShell ou o portal do Azure pode ser usado para configurar o que sincroniza neste servidor.</span><span class="sxs-lookup"><span data-stu-id="806e6-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="806e6-112">Um servidor só pode ser registrado em um único serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="806e6-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="806e6-113">Se os servidores precisarem participar da sincronização do mesmo conjunto de arquivos, registre-os no mesmo serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="806e6-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="806e6-114">O comando deve ser executado localmente no servidor que deve ser registrado, seja executado diretamente ou por meio de uma sessão remota do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="806e6-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="806e6-115">Não é possível aceitar um objeto de computador remoto.</span><span class="sxs-lookup"><span data-stu-id="806e6-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="806e6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="806e6-116">EXAMPLES</span></span>

### <span data-ttu-id="806e6-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="806e6-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="806e6-118">Esse comando registrará o servidor local em que este comando está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="806e6-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="806e6-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="806e6-119">PARAMETERS</span></span>

### <span data-ttu-id="806e6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="806e6-120">-AsJob</span></span>
<span data-ttu-id="806e6-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="806e6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="806e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806e6-122">-DefaultProfile</span></span>
<span data-ttu-id="806e6-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="806e6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="806e6-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="806e6-124">-ParentObject</span></span>
<span data-ttu-id="806e6-125">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="806e6-125">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="806e6-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="806e6-126">-ParentResourceId</span></span>
<span data-ttu-id="806e6-127">ID do Recurso Pai do StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="806e6-127">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806e6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806e6-128">-ResourceGroupName</span></span>
<span data-ttu-id="806e6-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="806e6-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806e6-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="806e6-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="806e6-131">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="806e6-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806e6-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="806e6-132">-Confirm</span></span>
<span data-ttu-id="806e6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="806e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="806e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806e6-134">-WhatIf</span></span>
<span data-ttu-id="806e6-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="806e6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="806e6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="806e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="806e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806e6-137">CommonParameters</span></span>
<span data-ttu-id="806e6-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806e6-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="806e6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806e6-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="806e6-140">INPUTS</span></span>

### <span data-ttu-id="806e6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="806e6-141">System.String</span></span>

### <span data-ttu-id="806e6-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="806e6-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="806e6-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="806e6-143">OUTPUTS</span></span>

### <span data-ttu-id="806e6-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="806e6-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="806e6-145">Notas</span><span class="sxs-lookup"><span data-stu-id="806e6-145">NOTES</span></span>

## <span data-ttu-id="806e6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="806e6-146">RELATED LINKS</span></span>
