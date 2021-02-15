---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112128"
---
# <span data-ttu-id="ef088-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="ef088-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="ef088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef088-102">SYNOPSIS</span></span>
<span data-ttu-id="ef088-103">Cria um objeto configurável de conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="ef088-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="ef088-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef088-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef088-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef088-105">DESCRIPTION</span></span>
<span data-ttu-id="ef088-106">Cria um objeto configurável de conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="ef088-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="ef088-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ef088-107">EXAMPLES</span></span>

### <span data-ttu-id="ef088-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef088-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="ef088-109">Cria conjunto de criptografia de disco usando a chave ativa determinada no cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="ef088-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="ef088-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef088-110">PARAMETERS</span></span>

### <span data-ttu-id="ef088-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef088-111">-DefaultProfile</span></span>
<span data-ttu-id="ef088-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef088-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef088-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="ef088-113">-EncryptionType</span></span>
<span data-ttu-id="ef088-114">Use-a para definir o tipo de criptografia do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="ef088-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="ef088-115">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span><span class="sxs-lookup"><span data-stu-id="ef088-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="ef088-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ef088-116">-IdentityType</span></span>
<span data-ttu-id="ef088-117">O tipo de Identidade Gerenciada usada pelo DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="ef088-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="ef088-118">Somente SystemAssigned tem suporte.</span><span class="sxs-lookup"><span data-stu-id="ef088-118">Only SystemAssigned is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef088-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="ef088-119">-KeyUrl</span></span>
<span data-ttu-id="ef088-120">URL apontando para a chave ativa no KeyVault</span><span class="sxs-lookup"><span data-stu-id="ef088-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="ef088-121">-Local</span><span class="sxs-lookup"><span data-stu-id="ef088-121">-Location</span></span>
<span data-ttu-id="ef088-122">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="ef088-122">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef088-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ef088-123">-SourceVaultId</span></span>
<span data-ttu-id="ef088-124">ID do recurso do KeyVault que contém a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="ef088-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef088-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef088-125">-Tag</span></span>
<span data-ttu-id="ef088-126">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ef088-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ef088-127">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ef088-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef088-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ef088-128">-Confirm</span></span>
<span data-ttu-id="ef088-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef088-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef088-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef088-130">-WhatIf</span></span>
<span data-ttu-id="ef088-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ef088-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef088-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef088-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef088-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef088-133">CommonParameters</span></span>
<span data-ttu-id="ef088-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef088-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef088-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef088-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef088-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ef088-136">INPUTS</span></span>

### <span data-ttu-id="ef088-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ef088-137">System.String</span></span>

### <span data-ttu-id="ef088-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ef088-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ef088-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="ef088-139">OUTPUTS</span></span>

### <span data-ttu-id="ef088-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ef088-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="ef088-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ef088-141">NOTES</span></span>

## <span data-ttu-id="ef088-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef088-142">RELATED LINKS</span></span>
