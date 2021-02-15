---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112485"
---
# <span data-ttu-id="a38aa-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a38aa-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="a38aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a38aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a38aa-103">Esse comando define o serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a38aa-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="a38aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a38aa-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a38aa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a38aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a38aa-106">Um serviço de sincronização de armazenamento é o recurso de nível superior para a Sincronização de Arquivos do Azure. Esse comando define o serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a38aa-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="a38aa-107">Recomendamos criar o menor serviço de sincronização de armazenamento que seja necessário para diferenciar grupos distintos de servidores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="a38aa-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="a38aa-108">Um serviço de sincronização de armazenamento contém grupos de sincronização e também funciona como um destino para registrar seus servidores.</span><span class="sxs-lookup"><span data-stu-id="a38aa-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="a38aa-109">Um servidor só pode ser registrado em um único serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a38aa-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="a38aa-110">Se os servidores precisarem participar da sincronização do mesmo conjunto de arquivos, registre-os no mesmo serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a38aa-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="a38aa-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a38aa-111">EXAMPLES</span></span>

### <span data-ttu-id="a38aa-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a38aa-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="a38aa-113">Esse comando definirá um serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a38aa-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="a38aa-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a38aa-114">PARAMETERS</span></span>

### <span data-ttu-id="a38aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38aa-115">-DefaultProfile</span></span>
<span data-ttu-id="a38aa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a38aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="a38aa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a38aa-117">-Name</span></span>
<span data-ttu-id="a38aa-118">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a38aa-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="a38aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a38aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="a38aa-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a38aa-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="a38aa-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="a38aa-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="a38aa-122">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="a38aa-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="a38aa-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="a38aa-123">-Tag</span></span>
<span data-ttu-id="a38aa-124">Marcas de Serviço de Sincronização de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a38aa-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="a38aa-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a38aa-125">-Confirm</span></span>
<span data-ttu-id="a38aa-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a38aa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a38aa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a38aa-127">-WhatIf</span></span>
<span data-ttu-id="a38aa-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a38aa-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a38aa-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a38aa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a38aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38aa-130">CommonParameters</span></span>
<span data-ttu-id="a38aa-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a38aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38aa-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a38aa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38aa-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="a38aa-133">INPUTS</span></span>

### <span data-ttu-id="a38aa-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a38aa-134">System.String</span></span>

## <span data-ttu-id="a38aa-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="a38aa-135">OUTPUTS</span></span>

### <span data-ttu-id="a38aa-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a38aa-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="a38aa-137">Notas</span><span class="sxs-lookup"><span data-stu-id="a38aa-137">NOTES</span></span>

## <span data-ttu-id="a38aa-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a38aa-138">RELATED LINKS</span></span>
