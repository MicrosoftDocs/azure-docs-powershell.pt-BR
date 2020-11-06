---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602511"
---
# <span data-ttu-id="bfff7-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="bfff7-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="bfff7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfff7-102">SYNOPSIS</span></span>
<span data-ttu-id="bfff7-103">Obtém informações sobre as redes gerenciadas pela recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="bfff7-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfff7-104">SYNTAX</span></span>

### <span data-ttu-id="bfff7-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bfff7-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfff7-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="bfff7-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfff7-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="bfff7-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfff7-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="bfff7-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfff7-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="bfff7-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfff7-110">ByName</span><span class="sxs-lookup"><span data-stu-id="bfff7-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfff7-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bfff7-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfff7-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfff7-112">DESCRIPTION</span></span>
<span data-ttu-id="bfff7-113">O cmdlet **Get-AzureRmSiteRecoveryNetwork** Obtém informações sobre as redes de recuperação de site do Azure para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="bfff7-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="bfff7-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfff7-114">EXAMPLES</span></span>

## <span data-ttu-id="bfff7-115">OS</span><span class="sxs-lookup"><span data-stu-id="bfff7-115">PARAMETERS</span></span>

### <span data-ttu-id="bfff7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfff7-116">-DefaultProfile</span></span>
<span data-ttu-id="bfff7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfff7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfff7-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="bfff7-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfff7-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bfff7-119">-FriendlyName</span></span>
<span data-ttu-id="bfff7-120">Especifica o nome amigável da rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfff7-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfff7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfff7-121">-Name</span></span>
<span data-ttu-id="bfff7-122">Especifica o nome da rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfff7-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfff7-123">-Servidor</span><span class="sxs-lookup"><span data-stu-id="bfff7-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfff7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfff7-124">CommonParameters</span></span>
<span data-ttu-id="bfff7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfff7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfff7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfff7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfff7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfff7-127">INPUTS</span></span>

### <span data-ttu-id="bfff7-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bfff7-128">ASRFabric</span></span>
<span data-ttu-id="bfff7-129">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="bfff7-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="bfff7-130">String</span><span class="sxs-lookup"><span data-stu-id="bfff7-130">String</span></span>
<span data-ttu-id="bfff7-131">O parâmetro ' FriendlyName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bfff7-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="bfff7-132">String</span><span class="sxs-lookup"><span data-stu-id="bfff7-132">String</span></span>
<span data-ttu-id="bfff7-133">O parâmetro ' FriendlyName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bfff7-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="bfff7-134">String</span><span class="sxs-lookup"><span data-stu-id="bfff7-134">String</span></span>
<span data-ttu-id="bfff7-135">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bfff7-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="bfff7-136">String</span><span class="sxs-lookup"><span data-stu-id="bfff7-136">String</span></span>
<span data-ttu-id="bfff7-137">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bfff7-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="bfff7-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="bfff7-138">ASRServer</span></span>
<span data-ttu-id="bfff7-139">O parâmetro ' Server ' aceita o valor do tipo ' ASRServer ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="bfff7-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="bfff7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfff7-140">OUTPUTS</span></span>

### <span data-ttu-id="bfff7-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="bfff7-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="bfff7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfff7-142">NOTES</span></span>

## <span data-ttu-id="bfff7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfff7-143">RELATED LINKS</span></span>

