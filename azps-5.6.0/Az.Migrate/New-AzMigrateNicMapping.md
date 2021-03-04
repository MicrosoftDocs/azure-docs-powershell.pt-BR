---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 9ec976cae2afc5070303404616b3615fe54e7b81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889231"
---
# <span data-ttu-id="608ca-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="608ca-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="608ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608ca-102">SYNOPSIS</span></span>
<span data-ttu-id="608ca-103">Cria um objeto para atualizar as propriedades NIC de um servidor replicante.</span><span class="sxs-lookup"><span data-stu-id="608ca-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="608ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="608ca-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="608ca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="608ca-105">DESCRIPTION</span></span>
<span data-ttu-id="608ca-106">O New-AzMigrateNicMapping cmdlet cria um mapeamento da NIC de origem anexada ao servidor a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="608ca-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="608ca-107">Esse objeto é fornecido como uma entrada para o cmdlet Set-AzMigrateServerReplication para atualizar o NIC e suas propriedades para um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="608ca-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="608ca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="608ca-108">EXAMPLES</span></span>

### <span data-ttu-id="608ca-109">Exemplo 1: Criar um objeto NIC</span><span class="sxs-lookup"><span data-stu-id="608ca-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="608ca-110">Cria um objeto de atualização NIC.</span><span class="sxs-lookup"><span data-stu-id="608ca-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="608ca-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="608ca-111">PARAMETERS</span></span>

### <span data-ttu-id="608ca-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="608ca-112">-NicID</span></span>
<span data-ttu-id="608ca-113">Especifica a ID da NIC a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="608ca-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ca-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="608ca-114">-TargetNicIP</span></span>
<span data-ttu-id="608ca-115">Especifica o IP dentro da sub-rede de destino a ser usada para a NIC.</span><span class="sxs-lookup"><span data-stu-id="608ca-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ca-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="608ca-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="608ca-117">Especifica se a NIC a ser atualizada será a principal, secundária ou não migrada.</span><span class="sxs-lookup"><span data-stu-id="608ca-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ca-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="608ca-118">-TargetNicSubnet</span></span>
<span data-ttu-id="608ca-119">Especifica o nome da Sub-rede para a NIC na Rede Virtual de destino para a qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="608ca-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="608ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608ca-120">CommonParameters</span></span>
<span data-ttu-id="608ca-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608ca-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="608ca-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608ca-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="608ca-123">INPUTS</span></span>

## <span data-ttu-id="608ca-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="608ca-124">OUTPUTS</span></span>

### <span data-ttu-id="608ca-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="608ca-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="608ca-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="608ca-126">NOTES</span></span>

<span data-ttu-id="608ca-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="608ca-127">ALIASES</span></span>

## <span data-ttu-id="608ca-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="608ca-128">RELATED LINKS</span></span>

