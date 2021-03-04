---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: f7b3f0924b1033f1c3b4ffd773ebbbbed985fa3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888135"
---
# <span data-ttu-id="0792c-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0792c-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="0792c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0792c-102">SYNOPSIS</span></span>
<span data-ttu-id="0792c-103">Este comando define o serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0792c-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="0792c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0792c-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0792c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0792c-105">DESCRIPTION</span></span>
<span data-ttu-id="0792c-106">Um serviço de sincronização de armazenamento é o recurso de nível superior para a Sincronização de Arquivos do Azure. Este comando define o serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0792c-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="0792c-107">Recomendamos criar tão poucos serviços de sincronização de armazenamento quanto absolutamente necessário para diferenciar grupos distintos de servidores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0792c-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="0792c-108">Um serviço de sincronização de armazenamento contém grupos de sincronização e também funciona como um destino para registrar seus servidores.</span><span class="sxs-lookup"><span data-stu-id="0792c-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="0792c-109">Um servidor só pode ser registrado em um único serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0792c-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="0792c-110">Se os servidores precisarem participar da sincronização do mesmo conjunto de arquivos, registre-os no mesmo serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0792c-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="0792c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0792c-111">EXAMPLES</span></span>

### <span data-ttu-id="0792c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0792c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="0792c-113">Este comando definirá um serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0792c-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="0792c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0792c-114">PARAMETERS</span></span>

### <span data-ttu-id="0792c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0792c-115">-DefaultProfile</span></span>
<span data-ttu-id="0792c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0792c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="0792c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0792c-117">-Name</span></span>
<span data-ttu-id="0792c-118">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0792c-118">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0792c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0792c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0792c-120">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="0792c-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0792c-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="0792c-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="0792c-122">IncomingTrafficPolicy do serviço de sincronização de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0792c-122">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0792c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="0792c-123">-Tag</span></span>
<span data-ttu-id="0792c-124">Marcas de serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0792c-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0792c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0792c-125">-Confirm</span></span>
<span data-ttu-id="0792c-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0792c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0792c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0792c-127">-WhatIf</span></span>
<span data-ttu-id="0792c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0792c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0792c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0792c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0792c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0792c-130">CommonParameters</span></span>
<span data-ttu-id="0792c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0792c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0792c-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0792c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0792c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0792c-133">INPUTS</span></span>

### <span data-ttu-id="0792c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0792c-134">System.String</span></span>

## <span data-ttu-id="0792c-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0792c-135">OUTPUTS</span></span>

### <span data-ttu-id="0792c-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0792c-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="0792c-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="0792c-137">NOTES</span></span>

## <span data-ttu-id="0792c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0792c-138">RELATED LINKS</span></span>
