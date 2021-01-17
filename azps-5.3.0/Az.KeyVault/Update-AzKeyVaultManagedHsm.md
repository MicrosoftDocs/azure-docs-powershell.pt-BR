---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429223"
---
# <span data-ttu-id="331ec-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="331ec-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="331ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="331ec-102">SYNOPSIS</span></span>
<span data-ttu-id="331ec-103">Atualize o estado de um HSM gerenciado do Azure.</span><span class="sxs-lookup"><span data-stu-id="331ec-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="331ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="331ec-104">SYNTAX</span></span>

### <span data-ttu-id="331ec-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="331ec-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331ec-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="331ec-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331ec-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="331ec-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331ec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="331ec-108">DESCRIPTION</span></span>
<span data-ttu-id="331ec-109">Esse cmdlet atualiza o estado de um HSM gerenciado do Azure.</span><span class="sxs-lookup"><span data-stu-id="331ec-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="331ec-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="331ec-110">EXAMPLES</span></span>

### <span data-ttu-id="331ec-111">Exemplo 1: atualizar um HSM gerenciado diretamente</span><span class="sxs-lookup"><span data-stu-id="331ec-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="331ec-112">Atualiza as marcas do HSM gerenciado nomeado `$hsmName` no grupo de recursos `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="331ec-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="331ec-113">Exemplo 2: atualizar um HSM gerenciado usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="331ec-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="331ec-114">Atualiza as marcas do HSM gerenciado usando a sintaxe de tubulação.</span><span class="sxs-lookup"><span data-stu-id="331ec-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="331ec-115">OS</span><span class="sxs-lookup"><span data-stu-id="331ec-115">PARAMETERS</span></span>

### <span data-ttu-id="331ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331ec-116">-DefaultProfile</span></span>
<span data-ttu-id="331ec-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="331ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="331ec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="331ec-118">-InputObject</span></span>
<span data-ttu-id="331ec-119">Objeto HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="331ec-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="331ec-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="331ec-120">-Name</span></span>
<span data-ttu-id="331ec-121">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="331ec-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="331ec-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="331ec-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331ec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="331ec-124">-ResourceId</span></span>
<span data-ttu-id="331ec-125">ID do recurso do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="331ec-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="331ec-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="331ec-126">-Tag</span></span>
<span data-ttu-id="331ec-127">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="331ec-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="331ec-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="331ec-128">-Confirm</span></span>
<span data-ttu-id="331ec-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="331ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="331ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="331ec-130">-WhatIf</span></span>
<span data-ttu-id="331ec-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="331ec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="331ec-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="331ec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="331ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331ec-133">CommonParameters</span></span>
<span data-ttu-id="331ec-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331ec-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="331ec-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331ec-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="331ec-136">INPUTS</span></span>

### <span data-ttu-id="331ec-137">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="331ec-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="331ec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="331ec-138">System.String</span></span>

### <span data-ttu-id="331ec-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="331ec-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="331ec-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="331ec-140">OUTPUTS</span></span>

### <span data-ttu-id="331ec-141">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="331ec-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="331ec-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="331ec-142">NOTES</span></span>

## <span data-ttu-id="331ec-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="331ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="331ec-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="331ec-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="331ec-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="331ec-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="331ec-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="331ec-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)