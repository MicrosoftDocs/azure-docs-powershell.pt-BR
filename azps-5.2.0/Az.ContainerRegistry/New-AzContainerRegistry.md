---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261208"
---
# <span data-ttu-id="c57ed-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57ed-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="c57ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c57ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c57ed-103">Cria um registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="c57ed-103">Creates a container registry.</span></span>

## <span data-ttu-id="c57ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c57ed-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c57ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c57ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c57ed-106">O cmdlet New-AzContainerRegistry cria um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c57ed-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c57ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c57ed-107">EXAMPLES</span></span>

### <span data-ttu-id="c57ed-108">Exemplo 1: criar um registro de contêiner com uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c57ed-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c57ed-109">Esse comando cria um registro de contêiner com uma nova conta de armazenamento no grupo MyResource do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c57ed-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="c57ed-110">Exemplo 2: criar um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="c57ed-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c57ed-111">Esse comando cria um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="c57ed-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="c57ed-112">OS</span><span class="sxs-lookup"><span data-stu-id="c57ed-112">PARAMETERS</span></span>

### <span data-ttu-id="c57ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57ed-113">-DefaultProfile</span></span>
<span data-ttu-id="c57ed-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c57ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c57ed-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c57ed-115">-EnableAdminUser</span></span>
<span data-ttu-id="c57ed-116">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c57ed-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="c57ed-117">-Local</span><span class="sxs-lookup"><span data-stu-id="c57ed-117">-Location</span></span>
<span data-ttu-id="c57ed-118">Local do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c57ed-118">Container Registry Location.</span></span>
<span data-ttu-id="c57ed-119">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c57ed-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c57ed-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c57ed-120">-Name</span></span>
<span data-ttu-id="c57ed-121">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c57ed-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="c57ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="c57ed-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c57ed-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c57ed-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="c57ed-124">-Sku</span></span>
<span data-ttu-id="c57ed-125">SKU do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c57ed-125">Container Registry SKU.</span></span>
<span data-ttu-id="c57ed-126">Valores permitidos: Basic.</span><span class="sxs-lookup"><span data-stu-id="c57ed-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c57ed-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="c57ed-127">-Tag</span></span>
<span data-ttu-id="c57ed-128">Marcas de registro de contêineres. pares de chave-valor na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c57ed-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="c57ed-129">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c57ed-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c57ed-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c57ed-130">-Confirm</span></span>
<span data-ttu-id="c57ed-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57ed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57ed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57ed-132">-WhatIf</span></span>
<span data-ttu-id="c57ed-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c57ed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c57ed-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c57ed-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57ed-135">CommonParameters</span></span>
<span data-ttu-id="c57ed-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c57ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57ed-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c57ed-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57ed-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c57ed-138">INPUTS</span></span>

### <span data-ttu-id="c57ed-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c57ed-139">System.String</span></span>

## <span data-ttu-id="c57ed-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c57ed-140">OUTPUTS</span></span>

### <span data-ttu-id="c57ed-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57ed-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c57ed-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c57ed-142">NOTES</span></span>

## <span data-ttu-id="c57ed-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c57ed-143">RELATED LINKS</span></span>

[<span data-ttu-id="c57ed-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57ed-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="c57ed-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57ed-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="c57ed-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57ed-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

