---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117727"
---
# <span data-ttu-id="7866e-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7866e-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="7866e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7866e-102">SYNOPSIS</span></span>
<span data-ttu-id="7866e-103">Obter HSMs gerenciados.</span><span class="sxs-lookup"><span data-stu-id="7866e-103">Get managed HSMs.</span></span>

## <span data-ttu-id="7866e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7866e-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7866e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7866e-105">DESCRIPTION</span></span>
<span data-ttu-id="7866e-106">O cmdlet **Get-AzManagedHsm** Obtém informações sobre os HSMs gerenciados em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="7866e-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="7866e-107">Você pode exibir todas as instâncias de HSMs gerenciadas em uma assinatura ou filtrar os resultados por um grupo de recursos ou HSM gerenciado específico.</span><span class="sxs-lookup"><span data-stu-id="7866e-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="7866e-108">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obtém um único HSM gerenciado, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="7866e-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="7866e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7866e-109">EXAMPLES</span></span>

### <span data-ttu-id="7866e-110">Exemplo 1: obter todos os HSMs gerenciados em sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="7866e-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7866e-111">Esse comando obtém todos os HSMs gerenciados na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7866e-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="7866e-112">Exemplo 2: obter um HSM gerenciado específico</span><span class="sxs-lookup"><span data-stu-id="7866e-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7866e-113">Este comando obtém o HSM gerenciado chamado myhsm na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7866e-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="7866e-114">Exemplo 3: obter HSMs gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7866e-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7866e-115">Esse comando obtém todos os HSMs gerenciados no grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="7866e-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="7866e-116">Exemplo 4: obter HSMs gerenciados usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="7866e-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7866e-117">Esse comando obtém todos os HSMs gerenciados na assinatura que começa com "myhsm".</span><span class="sxs-lookup"><span data-stu-id="7866e-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="7866e-118">OS</span><span class="sxs-lookup"><span data-stu-id="7866e-118">PARAMETERS</span></span>

### <span data-ttu-id="7866e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7866e-119">-DefaultProfile</span></span>
<span data-ttu-id="7866e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7866e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7866e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7866e-121">-Name</span></span>
<span data-ttu-id="7866e-122">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="7866e-122">HSM name.</span></span> <span data-ttu-id="7866e-123">O cmdlet constrói o FQDN de um HSM com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="7866e-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7866e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7866e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7866e-125">Especifica o nome do grupo de recursos associado ao HSM gerenciado que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="7866e-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7866e-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="7866e-126">-Tag</span></span>
<span data-ttu-id="7866e-127">Especifica a chave e o valor opcional da marca especificada para filtrar a lista de HSMs gerenciados por.</span><span class="sxs-lookup"><span data-stu-id="7866e-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="7866e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7866e-128">CommonParameters</span></span>
<span data-ttu-id="7866e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7866e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7866e-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7866e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7866e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7866e-131">INPUTS</span></span>

### <span data-ttu-id="7866e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7866e-132">System.String</span></span>

### <span data-ttu-id="7866e-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7866e-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7866e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7866e-134">OUTPUTS</span></span>

### <span data-ttu-id="7866e-135">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7866e-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="7866e-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7866e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="7866e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7866e-137">NOTES</span></span>

## <span data-ttu-id="7866e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7866e-138">RELATED LINKS</span></span>

[<span data-ttu-id="7866e-139">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7866e-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="7866e-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7866e-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="7866e-141">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7866e-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)