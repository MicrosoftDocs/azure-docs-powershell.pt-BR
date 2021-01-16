---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263556"
---
# <span data-ttu-id="d2c92-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d2c92-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="d2c92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2c92-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c92-103">Este comando define o serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2c92-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="d2c92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2c92-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2c92-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c92-106">Um serviço de sincronização de armazenamento é o recurso de nível superior da sincronização de arquivos do Azure. Este comando define o serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2c92-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="d2c92-107">Recomendamos que crie o menor número de serviços de sincronização de armazenamento que seja absolutamente necessário para diferenciar grupos distintos de servidores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="d2c92-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="d2c92-108">Um serviço de sincronização de armazenamento contém grupos de sincronização e também funciona como destino para registrar seus servidores em.</span><span class="sxs-lookup"><span data-stu-id="d2c92-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="d2c92-109">Um servidor somente pode ser registrado para um único serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d2c92-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="d2c92-110">Se os servidores já precisarem participar da sincronização do mesmo conjunto de arquivos, registre-os no mesmo serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d2c92-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="d2c92-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2c92-111">EXAMPLES</span></span>

### <span data-ttu-id="d2c92-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2c92-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="d2c92-113">Esse comando irá definir um serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d2c92-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="d2c92-114">OS</span><span class="sxs-lookup"><span data-stu-id="d2c92-114">PARAMETERS</span></span>

### <span data-ttu-id="d2c92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c92-115">-DefaultProfile</span></span>
<span data-ttu-id="d2c92-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="d2c92-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2c92-117">-Name</span></span>
<span data-ttu-id="d2c92-118">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d2c92-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="d2c92-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c92-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2c92-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2c92-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2c92-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c92-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="d2c92-122">Serviço de sincronização de IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c92-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="d2c92-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="d2c92-123">-Tag</span></span>
<span data-ttu-id="d2c92-124">Marcas de serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d2c92-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="d2c92-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2c92-125">-Confirm</span></span>
<span data-ttu-id="d2c92-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c92-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c92-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c92-127">-WhatIf</span></span>
<span data-ttu-id="d2c92-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2c92-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2c92-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2c92-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c92-130">CommonParameters</span></span>
<span data-ttu-id="d2c92-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c92-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c92-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c92-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2c92-133">INPUTS</span></span>

### <span data-ttu-id="d2c92-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d2c92-134">System.String</span></span>

## <span data-ttu-id="d2c92-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2c92-135">OUTPUTS</span></span>

### <span data-ttu-id="d2c92-136">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d2c92-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="d2c92-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2c92-137">NOTES</span></span>

## <span data-ttu-id="d2c92-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2c92-138">RELATED LINKS</span></span>
