---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773027"
---
# <span data-ttu-id="20c83-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="20c83-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="20c83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20c83-102">SYNOPSIS</span></span>
<span data-ttu-id="20c83-103">Obtém os detalhes dos provedores de serviços de recuperação ASR registrados no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="20c83-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="20c83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20c83-104">SYNTAX</span></span>

### <span data-ttu-id="20c83-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="20c83-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20c83-106">ByName</span><span class="sxs-lookup"><span data-stu-id="20c83-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c83-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="20c83-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c83-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20c83-108">DESCRIPTION</span></span>
<span data-ttu-id="20c83-109">O cmdlet **Get-AzRecoveryServicesAsrServicesProvider** Obtém informações sobre os provedores do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="20c83-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="20c83-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20c83-110">EXAMPLES</span></span>

### <span data-ttu-id="20c83-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20c83-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="20c83-112">Liste todos os provedores de serviços de replicação ASR registrados no cofre de serviços de recuperação correspondente à malha especificada.</span><span class="sxs-lookup"><span data-stu-id="20c83-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="20c83-113">OS</span><span class="sxs-lookup"><span data-stu-id="20c83-113">PARAMETERS</span></span>

### <span data-ttu-id="20c83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c83-114">-DefaultProfile</span></span>
<span data-ttu-id="20c83-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20c83-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="20c83-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="20c83-116">-Fabric</span></span>
<span data-ttu-id="20c83-117">Especifica o objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="20c83-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20c83-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="20c83-118">-FriendlyName</span></span>
<span data-ttu-id="20c83-119">Especifica o nome amigável do provedor de serviços de recuperação ASR para o qual obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="20c83-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c83-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="20c83-120">-Name</span></span>
<span data-ttu-id="20c83-121">Especifica o nome do provedor de serviços de recuperação ASR para o qual obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="20c83-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c83-122">CommonParameters</span></span>
<span data-ttu-id="20c83-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c83-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c83-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c83-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20c83-125">INPUTS</span></span>

### <span data-ttu-id="20c83-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="20c83-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="20c83-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20c83-127">OUTPUTS</span></span>

### <span data-ttu-id="20c83-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="20c83-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="20c83-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20c83-129">NOTES</span></span>

## <span data-ttu-id="20c83-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20c83-130">RELATED LINKS</span></span>

[<span data-ttu-id="20c83-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="20c83-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="20c83-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="20c83-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
