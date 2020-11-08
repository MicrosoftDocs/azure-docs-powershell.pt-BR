---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 1c546894cf9b11dcb65fb12b9b0575e2fd3191fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112398"
---
# <span data-ttu-id="c8289-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8289-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="c8289-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8289-102">SYNOPSIS</span></span>
<span data-ttu-id="c8289-103">Cria um registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="c8289-103">Creates a container registry.</span></span>

## <span data-ttu-id="c8289-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8289-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8289-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8289-105">DESCRIPTION</span></span>
<span data-ttu-id="c8289-106">O cmdlet New-AzContainerRegistry cria um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8289-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c8289-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8289-107">EXAMPLES</span></span>

### <span data-ttu-id="c8289-108">Exemplo 1: criar um registro de contêiner com uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8289-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c8289-109">Esse comando cria um registro de contêiner com uma nova conta de armazenamento no grupo MyResource do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c8289-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="c8289-110">Exemplo 2: criar um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="c8289-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c8289-111">Esse comando cria um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="c8289-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="c8289-112">Exemplo 3: criar um registro de contêiner com uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="c8289-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c8289-113">Esse comando cria um registro de contêiner com uma conta de armazenamento existente \` mystorageaccount \` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8289-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="c8289-114">OS</span><span class="sxs-lookup"><span data-stu-id="c8289-114">PARAMETERS</span></span>

### <span data-ttu-id="c8289-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8289-115">-DefaultProfile</span></span>
<span data-ttu-id="c8289-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c8289-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8289-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c8289-117">-EnableAdminUser</span></span>
<span data-ttu-id="c8289-118">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8289-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="c8289-119">-Local</span><span class="sxs-lookup"><span data-stu-id="c8289-119">-Location</span></span>
<span data-ttu-id="c8289-120">Local do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8289-120">Container Registry Location.</span></span>
<span data-ttu-id="c8289-121">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8289-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c8289-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8289-122">-Name</span></span>
<span data-ttu-id="c8289-123">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8289-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="c8289-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8289-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8289-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8289-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8289-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c8289-126">-Sku</span></span>
<span data-ttu-id="c8289-127">SKU do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8289-127">Container Registry SKU.</span></span>
<span data-ttu-id="c8289-128">Valores permitidos: Basic.</span><span class="sxs-lookup"><span data-stu-id="c8289-128">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="c8289-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8289-129">-StorageAccountName</span></span>
<span data-ttu-id="c8289-130">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="c8289-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="c8289-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="c8289-131">-Tag</span></span>
<span data-ttu-id="c8289-132">Marcas de registro de contêineres. pares de chave-valor na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c8289-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="c8289-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c8289-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8289-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8289-134">-Confirm</span></span>
<span data-ttu-id="c8289-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8289-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8289-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8289-136">-WhatIf</span></span>
<span data-ttu-id="c8289-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8289-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8289-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8289-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8289-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8289-139">CommonParameters</span></span>
<span data-ttu-id="c8289-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8289-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8289-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8289-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8289-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8289-142">INPUTS</span></span>

### <span data-ttu-id="c8289-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c8289-143">System.String</span></span>

## <span data-ttu-id="c8289-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8289-144">OUTPUTS</span></span>

### <span data-ttu-id="c8289-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8289-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c8289-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8289-146">NOTES</span></span>

## <span data-ttu-id="c8289-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8289-147">RELATED LINKS</span></span>

[<span data-ttu-id="c8289-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8289-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="c8289-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8289-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="c8289-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8289-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

