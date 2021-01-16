---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258880"
---
# <span data-ttu-id="46596-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="46596-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="46596-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46596-102">SYNOPSIS</span></span>
<span data-ttu-id="46596-103">Cria um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46596-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="46596-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46596-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46596-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46596-105">DESCRIPTION</span></span>
<span data-ttu-id="46596-106">O cmdlet **New-AzKeyVaultManagedHsm** cria um HSM gerenciado no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="46596-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="46596-107">Para adicionar, remover ou listar as chaves no HSM gerenciado, o usuário deve conceder permissões adicionando ID de usuário ao administrador.</span><span class="sxs-lookup"><span data-stu-id="46596-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="46596-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46596-108">EXAMPLES</span></span>

### <span data-ttu-id="46596-109">Exemplo 1: criar um HSM gerenciado StandardB1</span><span class="sxs-lookup"><span data-stu-id="46596-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="46596-110">Esse comando cria um HSM gerenciado chamado myhsm no local eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="46596-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="46596-111">O comando adiciona o HSM gerenciado ao grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="46596-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="46596-112">Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um Standard_B1 HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46596-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="46596-113">Exemplo 2: criar um HSM gerenciado CustomB32</span><span class="sxs-lookup"><span data-stu-id="46596-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="46596-114">Esse comando cria um HSM gerenciado, exatamente como o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="46596-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="46596-115">No entanto, ele especifica um valor de CustomB32 para o parâmetro *SKU* criar um HSM gerenciado CustomB32.</span><span class="sxs-lookup"><span data-stu-id="46596-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="46596-116">OS</span><span class="sxs-lookup"><span data-stu-id="46596-116">PARAMETERS</span></span>

### <span data-ttu-id="46596-117">-Administrador</span><span class="sxs-lookup"><span data-stu-id="46596-117">-Administrator</span></span>
<span data-ttu-id="46596-118">ID inicial do objeto do administrador para este pool gerenciado do HSM.</span><span class="sxs-lookup"><span data-stu-id="46596-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="46596-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46596-119">-AsJob</span></span>
<span data-ttu-id="46596-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="46596-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46596-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46596-121">-DefaultProfile</span></span>
<span data-ttu-id="46596-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46596-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46596-123">-Local</span><span class="sxs-lookup"><span data-stu-id="46596-123">-Location</span></span>
<span data-ttu-id="46596-124">Especifica a região do Azure na qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="46596-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="46596-125">Use o comando Get-AzResourceProvider com o parâmetro ProviderNamespace para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="46596-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="46596-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="46596-126">-Name</span></span>
<span data-ttu-id="46596-127">Especifica o nome do HSM gerenciado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="46596-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="46596-128">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="46596-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="46596-129">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="46596-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="46596-130">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="46596-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="46596-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46596-131">-ResourceGroupName</span></span>
<span data-ttu-id="46596-132">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="46596-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="46596-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="46596-133">-Sku</span></span>
<span data-ttu-id="46596-134">Especifica a SKU da instância do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46596-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="46596-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="46596-135">-Tag</span></span>
<span data-ttu-id="46596-136">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="46596-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="46596-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46596-137">-Confirm</span></span>
<span data-ttu-id="46596-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46596-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46596-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46596-139">-WhatIf</span></span>
<span data-ttu-id="46596-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46596-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46596-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46596-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46596-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46596-142">CommonParameters</span></span>
<span data-ttu-id="46596-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46596-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46596-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46596-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46596-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46596-145">INPUTS</span></span>

### <span data-ttu-id="46596-146">System. String</span><span class="sxs-lookup"><span data-stu-id="46596-146">System.String</span></span>

### <span data-ttu-id="46596-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="46596-147">System.String[]</span></span>

### <span data-ttu-id="46596-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="46596-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46596-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46596-149">OUTPUTS</span></span>

### <span data-ttu-id="46596-150">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="46596-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="46596-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46596-151">NOTES</span></span>

## <span data-ttu-id="46596-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46596-152">RELATED LINKS</span></span>

[<span data-ttu-id="46596-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="46596-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="46596-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="46596-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="46596-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="46596-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)