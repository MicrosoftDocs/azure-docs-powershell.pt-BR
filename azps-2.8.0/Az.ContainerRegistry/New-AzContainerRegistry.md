---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 6598f2f990567301a3604327a213696f4cc825dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597126"
---
# <span data-ttu-id="f98a4-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f98a4-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="f98a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f98a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f98a4-103">Cria um registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f98a4-103">Creates a container registry.</span></span>

## <span data-ttu-id="f98a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f98a4-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f98a4-105">DESCRIPTION</span></span>
<span data-ttu-id="f98a4-106">O cmdlet New-AzContainerRegistry cria um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f98a4-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="f98a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f98a4-107">EXAMPLES</span></span>

### <span data-ttu-id="f98a4-108">Exemplo 1: criar um registro de contêiner com uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f98a4-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f98a4-109">Esse comando cria um registro de contêiner com uma nova conta de armazenamento no grupo MyResource do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="f98a4-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="f98a4-110">Exemplo 2: criar um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="f98a4-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f98a4-111">Esse comando cria um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="f98a4-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="f98a4-112">Exemplo 3: criar um registro de contêiner com uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="f98a4-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f98a4-113">Esse comando cria um registro de contêiner com uma conta de armazenamento existente \` mystorageaccount \` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f98a4-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="f98a4-114">OS</span><span class="sxs-lookup"><span data-stu-id="f98a4-114">PARAMETERS</span></span>

### <span data-ttu-id="f98a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98a4-115">-DefaultProfile</span></span>
<span data-ttu-id="f98a4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f98a4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f98a4-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="f98a4-117">-EnableAdminUser</span></span>
<span data-ttu-id="f98a4-118">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f98a4-118">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98a4-119">-Local</span><span class="sxs-lookup"><span data-stu-id="f98a4-119">-Location</span></span>
<span data-ttu-id="f98a4-120">Local do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f98a4-120">Container Registry Location.</span></span>
<span data-ttu-id="f98a4-121">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f98a4-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="f98a4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f98a4-122">-Name</span></span>
<span data-ttu-id="f98a4-123">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f98a4-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f98a4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f98a4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f98a4-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="f98a4-126">-Sku</span></span>
<span data-ttu-id="f98a4-127">SKU do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f98a4-127">Container Registry SKU.</span></span>
<span data-ttu-id="f98a4-128">Valores permitidos: Basic.</span><span class="sxs-lookup"><span data-stu-id="f98a4-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98a4-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f98a4-129">-StorageAccountName</span></span>
<span data-ttu-id="f98a4-130">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="f98a4-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="f98a4-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="f98a4-131">-Tag</span></span>
<span data-ttu-id="f98a4-132">Marcas de registro de contêineres. pares de chave-valor na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f98a4-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="f98a4-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f98a4-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98a4-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f98a4-134">-Confirm</span></span>
<span data-ttu-id="f98a4-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f98a4-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98a4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98a4-136">-WhatIf</span></span>
<span data-ttu-id="f98a4-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f98a4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98a4-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f98a4-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98a4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98a4-139">CommonParameters</span></span>
<span data-ttu-id="f98a4-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98a4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98a4-141">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f98a4-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98a4-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f98a4-142">INPUTS</span></span>

### <span data-ttu-id="f98a4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f98a4-143">System.String</span></span>

## <span data-ttu-id="f98a4-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f98a4-144">OUTPUTS</span></span>

### <span data-ttu-id="f98a4-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f98a4-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f98a4-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f98a4-146">NOTES</span></span>

## <span data-ttu-id="f98a4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f98a4-147">RELATED LINKS</span></span>

[<span data-ttu-id="f98a4-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f98a4-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="f98a4-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f98a4-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="f98a4-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f98a4-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

