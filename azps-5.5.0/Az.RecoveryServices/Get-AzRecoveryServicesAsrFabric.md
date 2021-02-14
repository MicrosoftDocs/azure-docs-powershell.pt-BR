---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117236"
---
# <span data-ttu-id="bb351-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bb351-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="bb351-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb351-102">SYNOPSIS</span></span>
<span data-ttu-id="bb351-103">Obter os detalhes de uma Malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb351-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="bb351-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb351-104">SYNTAX</span></span>

### <span data-ttu-id="bb351-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb351-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb351-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bb351-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb351-107">ByName</span><span class="sxs-lookup"><span data-stu-id="bb351-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb351-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb351-108">DESCRIPTION</span></span>
<span data-ttu-id="bb351-109">O cmdlet **Get-AzRecoveryServicesAsrFabric** obtém as propriedades de um Malha de Recuperação de Site do Azure especificado ou todos os Azure Site Recovery Fabrics em um cofre do Serviço de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="bb351-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="bb351-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb351-110">EXAMPLES</span></span>

### <span data-ttu-id="bb351-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb351-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="bb351-112">Retorna todas as malhas de Recuperação de Site do Azure no cofre.</span><span class="sxs-lookup"><span data-stu-id="bb351-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="bb351-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bb351-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="bb351-114">Devolver a malha de recuperação do site do Azure com o nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="bb351-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="bb351-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bb351-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="bb351-116">Devolver a malha de recuperação de site do Azure com nome amigável xxxx.</span><span class="sxs-lookup"><span data-stu-id="bb351-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="bb351-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb351-117">PARAMETERS</span></span>

### <span data-ttu-id="bb351-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb351-118">-DefaultProfile</span></span>
<span data-ttu-id="bb351-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb351-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb351-120">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="bb351-120">-FriendlyName</span></span>
<span data-ttu-id="bb351-121">Pesquise a malha ASR pelo nome amigável do malha.</span><span class="sxs-lookup"><span data-stu-id="bb351-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="bb351-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb351-122">-Name</span></span>
<span data-ttu-id="bb351-123">Pesquise o malha ASR pelo nome da malha.</span><span class="sxs-lookup"><span data-stu-id="bb351-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="bb351-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb351-124">CommonParameters</span></span>
<span data-ttu-id="bb351-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb351-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb351-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb351-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb351-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb351-127">INPUTS</span></span>

### <span data-ttu-id="bb351-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bb351-128">None</span></span>

## <span data-ttu-id="bb351-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb351-129">OUTPUTS</span></span>

### <span data-ttu-id="bb351-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bb351-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bb351-131">Notas</span><span class="sxs-lookup"><span data-stu-id="bb351-131">NOTES</span></span>

## <span data-ttu-id="bb351-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb351-132">RELATED LINKS</span></span>

[<span data-ttu-id="bb351-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bb351-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="bb351-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bb351-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
