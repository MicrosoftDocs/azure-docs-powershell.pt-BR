---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441335"
---
# <span data-ttu-id="8cb25-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8cb25-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="8cb25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cb25-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb25-103">Obtém cofres de chave.</span><span class="sxs-lookup"><span data-stu-id="8cb25-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cb25-104">SYNTAX</span></span>

### <span data-ttu-id="8cb25-105">ListAllVaultsInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="8cb25-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cb25-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="8cb25-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cb25-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8cb25-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cb25-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="8cb25-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cb25-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cb25-109">DESCRIPTION</span></span>
<span data-ttu-id="8cb25-110">O cmdlet **Get-AzureRmKeyVault** Obtém informações sobre os cofres de chaves em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cb25-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="8cb25-111">Você pode exibir todas as instâncias de cofre de chaves em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um cofre de chaves específico.</span><span class="sxs-lookup"><span data-stu-id="8cb25-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="8cb25-112">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obtém um único cofre de chaves, você deve fazê-lo para obter melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="8cb25-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="8cb25-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cb25-113">EXAMPLES</span></span>

### <span data-ttu-id="8cb25-114">Exemplo 1: obter todos os cofres de chaves na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="8cb25-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="8cb25-115">Este comando obtém todos os cofres de chaves na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8cb25-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="8cb25-116">Exemplo 2: obter um cofre de chaves específico</span><span class="sxs-lookup"><span data-stu-id="8cb25-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="8cb25-117">Esse comando obtém o cofre de chaves chamado Contoso03Vault na sua assinatura atual e, em seguida, armazena-o na variável $MyVault.</span><span class="sxs-lookup"><span data-stu-id="8cb25-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="8cb25-118">Você pode inspecionar as propriedades de $MyVault para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8cb25-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="8cb25-119">Exemplo 3: obter cofres de chaves em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8cb25-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="8cb25-120">Esse comando obtém todos os cofres de chaves do grupo de recursos chamado ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8cb25-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="8cb25-121">Exemplo 4: obter todos os cofres de chaves excluídos na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="8cb25-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="8cb25-122">Este comando obtém todos os cofres de chaves excluídos na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8cb25-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="8cb25-123">Exemplo 5: obter um cofre de chaves excluído</span><span class="sxs-lookup"><span data-stu-id="8cb25-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="8cb25-124">Este comando obtém as informações de cofre de chave excluídas chamadas Contoso03Vault na sua assinatura atual e na região do eastus2.</span><span class="sxs-lookup"><span data-stu-id="8cb25-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="8cb25-125">OS</span><span class="sxs-lookup"><span data-stu-id="8cb25-125">PARAMETERS</span></span>

### <span data-ttu-id="8cb25-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb25-126">-DefaultProfile</span></span>
<span data-ttu-id="8cb25-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8cb25-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cb25-128">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="8cb25-128">-InRemovedState</span></span>
<span data-ttu-id="8cb25-129">Especifica se os cofres excluídos anteriormente devem ser mostrados na saída.</span><span class="sxs-lookup"><span data-stu-id="8cb25-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="8cb25-130">-Local</span><span class="sxs-lookup"><span data-stu-id="8cb25-130">-Location</span></span>
<span data-ttu-id="8cb25-131">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="8cb25-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb25-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb25-132">-ResourceGroupName</span></span>
<span data-ttu-id="8cb25-133">Especifica o nome do grupo de recursos associado ao cofre de chaves ou a cofres de chaves sendo consultados.</span><span class="sxs-lookup"><span data-stu-id="8cb25-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="8cb25-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="8cb25-134">-Tag</span></span>
<span data-ttu-id="8cb25-135">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8cb25-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8cb25-136">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8cb25-136">For example:</span></span>

<span data-ttu-id="8cb25-137">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8cb25-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8cb25-138">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8cb25-138">-VaultName</span></span>
<span data-ttu-id="8cb25-139">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8cb25-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb25-140">CommonParameters</span></span>
<span data-ttu-id="8cb25-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb25-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb25-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb25-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cb25-143">INPUTS</span></span>

### <span data-ttu-id="8cb25-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8cb25-144">None</span></span>
<span data-ttu-id="8cb25-145">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8cb25-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cb25-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cb25-146">OUTPUTS</span></span>

### <span data-ttu-id="8cb25-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8cb25-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8cb25-148">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="8cb25-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="8cb25-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="8cb25-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="8cb25-150">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="8cb25-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="8cb25-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cb25-151">NOTES</span></span>

## <span data-ttu-id="8cb25-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cb25-152">RELATED LINKS</span></span>

[<span data-ttu-id="8cb25-153">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8cb25-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="8cb25-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8cb25-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
