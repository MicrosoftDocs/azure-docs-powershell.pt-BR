---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775804"
---
# <span data-ttu-id="c7a92-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7a92-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="c7a92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7a92-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a92-103">Obtém cofres de chave.</span><span class="sxs-lookup"><span data-stu-id="c7a92-103">Gets key vaults.</span></span>

## <span data-ttu-id="c7a92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7a92-104">SYNTAX</span></span>

### <span data-ttu-id="c7a92-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="c7a92-105">GetVaultByName</span></span>
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a92-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c7a92-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a92-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7a92-107">ListVaultsByResourceGroup</span></span>
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7a92-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="c7a92-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a92-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="c7a92-109">ListAllVaultsInSubscription</span></span>
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a92-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7a92-110">DESCRIPTION</span></span>
<span data-ttu-id="c7a92-111">O cmdlet **Get-AzKeyVault** Obtém informações sobre os cofres de chaves em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7a92-111">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="c7a92-112">Você pode exibir todas as instâncias de cofre de chaves em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um cofre de chaves específico.</span><span class="sxs-lookup"><span data-stu-id="c7a92-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="c7a92-113">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obtém um único cofre de chaves, você deve fazê-lo para obter melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="c7a92-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="c7a92-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7a92-114">EXAMPLES</span></span>

### <span data-ttu-id="c7a92-115">Exemplo 1: obter todos os cofres de chaves na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="c7a92-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault
```

<span data-ttu-id="c7a92-116">Este comando obtém todos os cofres de chaves na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c7a92-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="c7a92-117">Exemplo 2: obter um cofre de chaves específico</span><span class="sxs-lookup"><span data-stu-id="c7a92-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="c7a92-118">Esse comando obtém o cofre de chaves chamado Contoso03Vault na sua assinatura atual e, em seguida, armazena-o na variável $MyVault.</span><span class="sxs-lookup"><span data-stu-id="c7a92-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="c7a92-119">Você pode inspecionar as propriedades de $MyVault para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="c7a92-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="c7a92-120">Exemplo 3: obter cofres de chaves em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c7a92-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="c7a92-121">Esse comando obtém todos os cofres de chaves do grupo de recursos chamado ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c7a92-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="c7a92-122">Exemplo 4: obter todos os cofres de chaves excluídos na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="c7a92-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault -InRemovedState
```

<span data-ttu-id="c7a92-123">Este comando obtém todos os cofres de chaves excluídos na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c7a92-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="c7a92-124">Exemplo 5: obter um cofre de chaves excluído</span><span class="sxs-lookup"><span data-stu-id="c7a92-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="c7a92-125">Este comando obtém as informações de cofre de chave excluídas chamadas Contoso03Vault na sua assinatura atual e na região do eastus2.</span><span class="sxs-lookup"><span data-stu-id="c7a92-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="c7a92-126">OS</span><span class="sxs-lookup"><span data-stu-id="c7a92-126">PARAMETERS</span></span>

### <span data-ttu-id="c7a92-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a92-127">-DefaultProfile</span></span>
<span data-ttu-id="c7a92-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c7a92-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a92-129">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="c7a92-129">-InRemovedState</span></span>
<span data-ttu-id="c7a92-130">Especifica se os cofres excluídos anteriormente devem ser mostrados na saída.</span><span class="sxs-lookup"><span data-stu-id="c7a92-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a92-131">-Local</span><span class="sxs-lookup"><span data-stu-id="c7a92-131">-Location</span></span>
<span data-ttu-id="c7a92-132">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="c7a92-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a92-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a92-133">-ResourceGroupName</span></span>
<span data-ttu-id="c7a92-134">Especifica o nome do grupo de recursos associado ao cofre de chaves ou a cofres de chaves sendo consultados.</span><span class="sxs-lookup"><span data-stu-id="c7a92-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a92-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="c7a92-135">-Tag</span></span>
<span data-ttu-id="c7a92-136">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c7a92-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7a92-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c7a92-137">For example:</span></span>

<span data-ttu-id="c7a92-138">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c7a92-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a92-139">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="c7a92-139">-VaultName</span></span>
<span data-ttu-id="c7a92-140">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="c7a92-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a92-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a92-141">CommonParameters</span></span>
<span data-ttu-id="c7a92-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a92-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a92-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a92-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a92-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7a92-144">INPUTS</span></span>

### <span data-ttu-id="c7a92-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c7a92-145">None</span></span>
<span data-ttu-id="c7a92-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c7a92-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7a92-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7a92-147">OUTPUTS</span></span>

### <span data-ttu-id="c7a92-148">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="c7a92-148">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="c7a92-149">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="c7a92-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="c7a92-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c7a92-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="c7a92-151">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="c7a92-151">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="c7a92-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7a92-152">NOTES</span></span>

## <span data-ttu-id="c7a92-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7a92-153">RELATED LINKS</span></span>

[<span data-ttu-id="c7a92-154">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7a92-154">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="c7a92-155">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7a92-155">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
