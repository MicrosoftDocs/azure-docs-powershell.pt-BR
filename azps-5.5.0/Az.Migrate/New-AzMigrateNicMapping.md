---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117550"
---
# <span data-ttu-id="74fcd-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="74fcd-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="74fcd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="74fcd-103">Cria um objeto para atualizar as propriedades NIC de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="74fcd-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="74fcd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74fcd-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="74fcd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="74fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="74fcd-106">O New-AzMigrateNicMapping cmdlet cria um mapeamento da fonte NIC anexada ao servidor a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="74fcd-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="74fcd-107">Este objeto é fornecido como uma entrada para o cmdlet Set-AzMigrateServerReplication atualizar a NIC e suas propriedades para um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="74fcd-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="74fcd-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74fcd-108">EXAMPLES</span></span>

### <span data-ttu-id="74fcd-109">Exemplo 1: Criar um objeto NIC</span><span class="sxs-lookup"><span data-stu-id="74fcd-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="74fcd-110">Cria um objeto de atualização NIC.</span><span class="sxs-lookup"><span data-stu-id="74fcd-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="74fcd-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74fcd-111">PARAMETERS</span></span>

### <span data-ttu-id="74fcd-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="74fcd-112">-NicID</span></span>
<span data-ttu-id="74fcd-113">Especifica a ID da NIC a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="74fcd-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="74fcd-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="74fcd-114">-TargetNicIP</span></span>
<span data-ttu-id="74fcd-115">Especifica o IP dentro da sub-rede de destino a ser usado para a NIC.</span><span class="sxs-lookup"><span data-stu-id="74fcd-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="74fcd-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="74fcd-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="74fcd-117">Especifica se a NIC a ser atualizada será a principal, secundária ou não migrada.</span><span class="sxs-lookup"><span data-stu-id="74fcd-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="74fcd-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="74fcd-118">-TargetNicSubnet</span></span>
<span data-ttu-id="74fcd-119">Especifica o nome da Sub-rede da NIC na Rede Virtual de destino para a qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="74fcd-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="74fcd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fcd-120">CommonParameters</span></span>
<span data-ttu-id="74fcd-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fcd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fcd-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74fcd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fcd-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="74fcd-123">INPUTS</span></span>

## <span data-ttu-id="74fcd-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="74fcd-124">OUTPUTS</span></span>

### <span data-ttu-id="74fcd-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="74fcd-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="74fcd-126">Notas</span><span class="sxs-lookup"><span data-stu-id="74fcd-126">NOTES</span></span>

<span data-ttu-id="74fcd-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="74fcd-127">ALIASES</span></span>

## <span data-ttu-id="74fcd-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74fcd-128">RELATED LINKS</span></span>

