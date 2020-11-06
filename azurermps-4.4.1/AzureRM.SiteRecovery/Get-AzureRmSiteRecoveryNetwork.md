---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429078"
---
# <span data-ttu-id="15ef3-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="15ef3-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="15ef3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="15ef3-103">Obtém informações sobre as redes gerenciadas pela recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="15ef3-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15ef3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15ef3-104">SYNTAX</span></span>

### <span data-ttu-id="15ef3-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="15ef3-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15ef3-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="15ef3-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15ef3-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="15ef3-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15ef3-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="15ef3-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15ef3-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="15ef3-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15ef3-110">ByName</span><span class="sxs-lookup"><span data-stu-id="15ef3-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15ef3-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="15ef3-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15ef3-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15ef3-112">DESCRIPTION</span></span>
<span data-ttu-id="15ef3-113">O cmdlet **Get-AzureRmSiteRecoveryNetwork** Obtém informações sobre as redes de recuperação de site do Azure para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="15ef3-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="15ef3-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15ef3-114">EXAMPLES</span></span>

## <span data-ttu-id="15ef3-115">OS</span><span class="sxs-lookup"><span data-stu-id="15ef3-115">PARAMETERS</span></span>

### <span data-ttu-id="15ef3-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="15ef3-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ef3-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="15ef3-117">-FriendlyName</span></span>
<span data-ttu-id="15ef3-118">Especifica o nome amigável da rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="15ef3-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ef3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="15ef3-119">-Name</span></span>
<span data-ttu-id="15ef3-120">Especifica o nome da rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="15ef3-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ef3-121">-Servidor</span><span class="sxs-lookup"><span data-stu-id="15ef3-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ef3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ef3-122">-DefaultProfile</span></span>
<span data-ttu-id="15ef3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15ef3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ef3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ef3-124">CommonParameters</span></span>
<span data-ttu-id="15ef3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15ef3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ef3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15ef3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ef3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15ef3-127">INPUTS</span></span>

### <span data-ttu-id="15ef3-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="15ef3-128">ASRFabric</span></span>
<span data-ttu-id="15ef3-129">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="15ef3-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="15ef3-130">String</span><span class="sxs-lookup"><span data-stu-id="15ef3-130">String</span></span>
<span data-ttu-id="15ef3-131">O parâmetro ' FriendlyName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="15ef3-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="15ef3-132">String</span><span class="sxs-lookup"><span data-stu-id="15ef3-132">String</span></span>
<span data-ttu-id="15ef3-133">O parâmetro ' FriendlyName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="15ef3-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="15ef3-134">String</span><span class="sxs-lookup"><span data-stu-id="15ef3-134">String</span></span>
<span data-ttu-id="15ef3-135">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="15ef3-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="15ef3-136">String</span><span class="sxs-lookup"><span data-stu-id="15ef3-136">String</span></span>
<span data-ttu-id="15ef3-137">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="15ef3-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="15ef3-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="15ef3-138">ASRServer</span></span>
<span data-ttu-id="15ef3-139">O parâmetro ' Server ' aceita o valor do tipo ' ASRServer ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="15ef3-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="15ef3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15ef3-140">OUTPUTS</span></span>

### <span data-ttu-id="15ef3-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="15ef3-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="15ef3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15ef3-142">NOTES</span></span>

## <span data-ttu-id="15ef3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15ef3-143">RELATED LINKS</span></span>

