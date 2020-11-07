---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 2913cbece59687516aa7e2aa83e3cea035218fd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774313"
---
# <span data-ttu-id="3e8cb-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3e8cb-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="3e8cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8cb-103">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="3e8cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e8cb-104">SYNTAX</span></span>

### <span data-ttu-id="3e8cb-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e8cb-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8cb-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="3e8cb-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8cb-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e8cb-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8cb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e8cb-108">DESCRIPTION</span></span>
<span data-ttu-id="3e8cb-109">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="3e8cb-110">Um grupo de sincronização é usado para descrever uma topologia de locais, chamadas de pontos de extremidade, que sincronizarão todos os arquivos armazenados em qualquer um dos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="3e8cb-111">Um grupo de sincronização contém pontos de extremidade de nuvem, que fazem referência a compartilhamentos de arquivos do Azure, e também contém pontos de extremidade do servidor que fazem referência a um caminho local específico em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="3e8cb-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e8cb-112">EXAMPLES</span></span>

### <span data-ttu-id="3e8cb-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e8cb-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="3e8cb-114">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="3e8cb-115">OS</span><span class="sxs-lookup"><span data-stu-id="3e8cb-115">PARAMETERS</span></span>

### <span data-ttu-id="3e8cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8cb-116">-DefaultProfile</span></span>
<span data-ttu-id="3e8cb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e8cb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e8cb-118">-Name</span></span>
<span data-ttu-id="3e8cb-119">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8cb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3e8cb-120">-ParentObject</span></span>
<span data-ttu-id="3e8cb-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3e8cb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3e8cb-122">-ParentResourceId</span></span>
<span data-ttu-id="3e8cb-123">ID do recurso pai StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3e8cb-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="3e8cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e8cb-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e8cb-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3e8cb-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="3e8cb-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3e8cb-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e8cb-128">-Confirm</span></span>
<span data-ttu-id="3e8cb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8cb-130">-WhatIf</span></span>
<span data-ttu-id="3e8cb-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e8cb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8cb-133">CommonParameters</span></span>
<span data-ttu-id="3e8cb-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8cb-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8cb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8cb-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e8cb-136">INPUTS</span></span>

### <span data-ttu-id="3e8cb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3e8cb-137">System.String</span></span>

### <span data-ttu-id="3e8cb-138">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3e8cb-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="3e8cb-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e8cb-139">OUTPUTS</span></span>

### <span data-ttu-id="3e8cb-140">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3e8cb-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="3e8cb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e8cb-141">NOTES</span></span>

## <span data-ttu-id="3e8cb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e8cb-142">RELATED LINKS</span></span>
