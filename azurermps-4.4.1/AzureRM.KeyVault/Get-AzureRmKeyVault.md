---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427917"
---
# <span data-ttu-id="06d9d-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="06d9d-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="06d9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="06d9d-103">Obtém cofres de chave.</span><span class="sxs-lookup"><span data-stu-id="06d9d-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06d9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06d9d-104">SYNTAX</span></span>

### <span data-ttu-id="06d9d-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="06d9d-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d9d-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="06d9d-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d9d-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06d9d-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06d9d-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="06d9d-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d9d-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="06d9d-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d9d-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06d9d-110">DESCRIPTION</span></span>
<span data-ttu-id="06d9d-111">O cmdlet **Get-AzureRmKeyVault** Obtém informações sobre os cofres de chaves em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="06d9d-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="06d9d-112">Você pode exibir todas as instâncias de cofre de chaves em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um cofre de chaves específico.</span><span class="sxs-lookup"><span data-stu-id="06d9d-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="06d9d-113">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obtém um único cofre de chaves, você deve fazê-lo para obter melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="06d9d-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="06d9d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06d9d-114">EXAMPLES</span></span>

### <span data-ttu-id="06d9d-115">Exemplo 1: obter todos os cofres de chaves na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="06d9d-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="06d9d-116">Este comando obtém todos os cofres de chaves na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="06d9d-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="06d9d-117">Exemplo 2: obter um cofre de chaves específico</span><span class="sxs-lookup"><span data-stu-id="06d9d-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="06d9d-118">Esse comando obtém o cofre de chaves chamado Contoso03Vault na sua assinatura atual e, em seguida, armazena-o na variável $MyVault.</span><span class="sxs-lookup"><span data-stu-id="06d9d-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="06d9d-119">Você pode inspecionar as propriedades de $MyVault para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="06d9d-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="06d9d-120">Exemplo 3: obter cofres de chaves em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="06d9d-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="06d9d-121">Esse comando obtém todos os cofres de chaves do grupo de recursos chamado ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="06d9d-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="06d9d-122">Exemplo 4: obter todos os cofres de chaves excluídos na sua assinatura atual</span><span class="sxs-lookup"><span data-stu-id="06d9d-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="06d9d-123">Este comando obtém todos os cofres de chaves excluídos na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="06d9d-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="06d9d-124">Exemplo 5: obter um cofre de chaves excluído</span><span class="sxs-lookup"><span data-stu-id="06d9d-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="06d9d-125">Este comando obtém as informações de cofre de chave excluídas chamadas Contoso03Vault na sua assinatura atual e na região do eastus2.</span><span class="sxs-lookup"><span data-stu-id="06d9d-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="06d9d-126">OS</span><span class="sxs-lookup"><span data-stu-id="06d9d-126">PARAMETERS</span></span>

### <span data-ttu-id="06d9d-127">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="06d9d-127">-InRemovedState</span></span>
<span data-ttu-id="06d9d-128">Especifica se os cofres excluídos anteriormente devem ser mostrados na saída.</span><span class="sxs-lookup"><span data-stu-id="06d9d-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d9d-129">-Local</span><span class="sxs-lookup"><span data-stu-id="06d9d-129">-Location</span></span>
<span data-ttu-id="06d9d-130">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="06d9d-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d9d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d9d-131">-ResourceGroupName</span></span>
<span data-ttu-id="06d9d-132">Especifica o nome do grupo de recursos associado ao cofre de chaves ou a cofres de chaves sendo consultados.</span><span class="sxs-lookup"><span data-stu-id="06d9d-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d9d-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="06d9d-133">-Tag</span></span>
<span data-ttu-id="06d9d-134">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="06d9d-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06d9d-135">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="06d9d-135">For example:</span></span>

<span data-ttu-id="06d9d-136">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="06d9d-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d9d-137">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="06d9d-137">-VaultName</span></span>
<span data-ttu-id="06d9d-138">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="06d9d-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d9d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d9d-139">-DefaultProfile</span></span>
<span data-ttu-id="06d9d-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06d9d-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d9d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d9d-141">CommonParameters</span></span>
<span data-ttu-id="06d9d-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d9d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d9d-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d9d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d9d-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06d9d-144">INPUTS</span></span>

## <span data-ttu-id="06d9d-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06d9d-145">OUTPUTS</span></span>

### <span data-ttu-id="06d9d-146">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="06d9d-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="06d9d-147">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="06d9d-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="06d9d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="06d9d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="06d9d-149">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="06d9d-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="06d9d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06d9d-150">NOTES</span></span>

## <span data-ttu-id="06d9d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06d9d-151">RELATED LINKS</span></span>

[<span data-ttu-id="06d9d-152">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="06d9d-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="06d9d-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="06d9d-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
