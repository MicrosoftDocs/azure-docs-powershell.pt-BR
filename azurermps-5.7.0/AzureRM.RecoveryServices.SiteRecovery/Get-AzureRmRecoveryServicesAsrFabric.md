---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 92631a1a6c5d27953777efe2b6ea158f59da8fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427471"
---
# <span data-ttu-id="3f333-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3f333-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="3f333-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f333-102">SYNOPSIS</span></span>
<span data-ttu-id="3f333-103">Obtenha os detalhes de uma malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f333-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f333-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f333-104">SYNTAX</span></span>

### <span data-ttu-id="3f333-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f333-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f333-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3f333-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f333-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f333-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f333-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f333-108">DESCRIPTION</span></span>
<span data-ttu-id="3f333-109">O cmdlet **Get-AzureRmRecoveryServicesAsrFabric** Obtém as propriedades de uma malha de recuperação de site do Azure especificada ou todas as malhas do Azure site Recovery em um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3f333-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="3f333-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f333-110">EXAMPLES</span></span>

### <span data-ttu-id="3f333-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f333-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="3f333-112">Retorna todas as malhas do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="3f333-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="3f333-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3f333-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="3f333-114">Retorne a malha do Azure site Recovery com o nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="3f333-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="3f333-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3f333-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="3f333-116">Retorne a estrutura do Azure site Recovery com o nome amigável xxxx.</span><span class="sxs-lookup"><span data-stu-id="3f333-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="3f333-117">OS</span><span class="sxs-lookup"><span data-stu-id="3f333-117">PARAMETERS</span></span>

### <span data-ttu-id="3f333-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f333-118">-DefaultProfile</span></span>
<span data-ttu-id="3f333-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f333-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="3f333-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f333-120">-FriendlyName</span></span>
<span data-ttu-id="3f333-121">Procure a malha ASR pelo nome amigável da malha.</span><span class="sxs-lookup"><span data-stu-id="3f333-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f333-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f333-122">-Name</span></span>
<span data-ttu-id="3f333-123">Procure a malha ASR pelo nome da malha.</span><span class="sxs-lookup"><span data-stu-id="3f333-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f333-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f333-124">CommonParameters</span></span>
<span data-ttu-id="3f333-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f333-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f333-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f333-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f333-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f333-127">INPUTS</span></span>

### <span data-ttu-id="3f333-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3f333-128">None</span></span>

## <span data-ttu-id="3f333-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f333-129">OUTPUTS</span></span>

### <span data-ttu-id="3f333-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3f333-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f333-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f333-131">NOTES</span></span>

## <span data-ttu-id="3f333-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f333-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f333-133">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3f333-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="3f333-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3f333-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)