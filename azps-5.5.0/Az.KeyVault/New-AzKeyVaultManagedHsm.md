---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113106"
---
# <span data-ttu-id="e0ab3-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ab3-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="e0ab3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ab3-103">Cria um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="e0ab3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0ab3-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ab3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ab3-106">O cmdlet **New-AzKeyVaultManagedHsm** cria um HSM gerenciado no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="e0ab3-107">Para adicionar, remover ou listar chaves no HSM gerenciado, o usuário deve conceder permissões adicionando a ID de usuário ao Administrador.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="e0ab3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0ab3-108">EXAMPLES</span></span>

### <span data-ttu-id="e0ab3-109">Exemplo 1: Criar um HSM gerenciado pelo StandardB1</span><span class="sxs-lookup"><span data-stu-id="e0ab3-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e0ab3-110">Esse comando cria um HSM gerenciado chamado myhsm no local eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="e0ab3-111">O comando adiciona o HSM gerenciado ao grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="e0ab3-112">Como o comando não especifica um valor para o parâmetro *SKU,* ele cria uma Standard_B1 HSM gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="e0ab3-113">Exemplo 2: Criar um HSM gerenciado personalizadoB32</span><span class="sxs-lookup"><span data-stu-id="e0ab3-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="e0ab3-114">Esse comando cria um HSM gerenciado, assim como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="e0ab3-115">No entanto, especifica um valor de CustomB32 para o parâmetro *SKU* para criar um HSM gerenciado por CustomB32.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="e0ab3-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0ab3-116">PARAMETERS</span></span>

### <span data-ttu-id="e0ab3-117">-Administrador</span><span class="sxs-lookup"><span data-stu-id="e0ab3-117">-Administrator</span></span>
<span data-ttu-id="e0ab3-118">ID do objeto de administrador inicial para este pool de HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ab3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0ab3-119">-AsJob</span></span>
<span data-ttu-id="e0ab3-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e0ab3-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ab3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ab3-121">-DefaultProfile</span></span>
<span data-ttu-id="e0ab3-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ab3-123">-Local</span><span class="sxs-lookup"><span data-stu-id="e0ab3-123">-Location</span></span>
<span data-ttu-id="e0ab3-124">Especifica a região do Azure na qual criar o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="e0ab3-125">Use o comando Get-AzResourceProvider com o parâmetro ProviderNamespace para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ab3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0ab3-126">-Name</span></span>
<span data-ttu-id="e0ab3-127">Especifica um nome do HSM gerenciado para criar.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="e0ab3-128">O nome pode ser qualquer combinação de letras, dígitos ou hífens.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="e0ab3-129">O nome deve começar e terminar com uma letra ou dígito.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="e0ab3-130">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ab3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ab3-131">-ResourceGroupName</span></span>
<span data-ttu-id="e0ab3-132">Especifica o nome de um grupo de recursos existente no qual se cria o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ab3-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="e0ab3-133">-Sku</span></span>
<span data-ttu-id="e0ab3-134">Especifica a SKU da instância HSM gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ab3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0ab3-135">-Tag</span></span>
<span data-ttu-id="e0ab3-136">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e0ab3-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0ab3-137">-Confirm</span></span>
<span data-ttu-id="e0ab3-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ab3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ab3-139">-WhatIf</span></span>
<span data-ttu-id="e0ab3-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ab3-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ab3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ab3-142">CommonParameters</span></span>
<span data-ttu-id="e0ab3-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ab3-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ab3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ab3-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0ab3-145">INPUTS</span></span>

### <span data-ttu-id="e0ab3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ab3-146">System.String</span></span>

### <span data-ttu-id="e0ab3-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e0ab3-147">System.String[]</span></span>

### <span data-ttu-id="e0ab3-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0ab3-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0ab3-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0ab3-149">OUTPUTS</span></span>

### <span data-ttu-id="e0ab3-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ab3-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="e0ab3-151">Notas</span><span class="sxs-lookup"><span data-stu-id="e0ab3-151">NOTES</span></span>

## <span data-ttu-id="e0ab3-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0ab3-152">RELATED LINKS</span></span>

[<span data-ttu-id="e0ab3-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ab3-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="e0ab3-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ab3-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="e0ab3-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ab3-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)