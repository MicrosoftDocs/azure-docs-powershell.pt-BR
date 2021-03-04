---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: b65fed5670f34072504c736283ba12e51086d3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891019"
---
# <span data-ttu-id="1d9e1-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1d9e1-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="1d9e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9e1-103">Obter HSMs gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-103">Get managed HSMs.</span></span>

## <span data-ttu-id="1d9e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d9e1-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9e1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d9e1-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9e1-106">O cmdlet **Get-AzKeyVaultManagedHsm** obtém informações sobre as HSMs gerenciadas em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="1d9e1-107">Você pode exibir todas as instâncias HSMs gerenciadas em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um HSM gerenciado específico.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="1d9e1-108">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obter um único HSM gerenciado, você deve fazer isso para obter um desempenho melhor.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="1d9e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d9e1-109">EXAMPLES</span></span>

### <span data-ttu-id="1d9e1-110">Exemplo 1: Obter todas as HSMs gerenciadas em sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="1d9e1-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1d9e1-111">Esse comando obtém todas as HSMs gerenciadas em sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="1d9e1-112">Exemplo 2: Obter um HSM gerenciado específico</span><span class="sxs-lookup"><span data-stu-id="1d9e1-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1d9e1-113">Este comando obtém o HSM gerenciado chamado myhsm em sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="1d9e1-114">Exemplo 3: Obter HSMs gerenciadas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1d9e1-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1d9e1-115">Este comando obtém todas as HSMs gerenciadas no grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="1d9e1-116">Exemplo 4: Obter HSMs gerenciadas usando filtragem</span><span class="sxs-lookup"><span data-stu-id="1d9e1-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1d9e1-117">Esse comando obtém todas as HSMs gerenciadas na assinatura que começam com "myhsm".</span><span class="sxs-lookup"><span data-stu-id="1d9e1-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="1d9e1-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d9e1-118">PARAMETERS</span></span>

### <span data-ttu-id="1d9e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9e1-119">-DefaultProfile</span></span>
<span data-ttu-id="1d9e1-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d9e1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1d9e1-121">-Name</span></span>
<span data-ttu-id="1d9e1-122">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-122">HSM name.</span></span> <span data-ttu-id="1d9e1-123">O cmdlet constrói o FQDN de um HSM com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1d9e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d9e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d9e1-125">Especifica o nome do grupo de recursos associado ao HSM gerenciado que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1d9e1-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d9e1-126">-Tag</span></span>
<span data-ttu-id="1d9e1-127">Especifica a chave e o valor opcional da marca especificada para filtrar a lista de HSMs gerenciadas por.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d9e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9e1-128">CommonParameters</span></span>
<span data-ttu-id="1d9e1-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9e1-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d9e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9e1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d9e1-131">INPUTS</span></span>

### <span data-ttu-id="1d9e1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1d9e1-132">System.String</span></span>

### <span data-ttu-id="1d9e1-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1d9e1-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1d9e1-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d9e1-134">OUTPUTS</span></span>

### <span data-ttu-id="1d9e1-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1d9e1-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="1d9e1-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1d9e1-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="1d9e1-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d9e1-137">NOTES</span></span>

## <span data-ttu-id="1d9e1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d9e1-138">RELATED LINKS</span></span>

[<span data-ttu-id="1d9e1-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1d9e1-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1d9e1-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1d9e1-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1d9e1-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1d9e1-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)