---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 4d9b788637e0c97d8f129df33ac7e4050ce916d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886784"
---
# <span data-ttu-id="3d848-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d848-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="3d848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d848-102">SYNOPSIS</span></span>
<span data-ttu-id="3d848-103">Cria um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d848-103">Creates a container registry.</span></span>

## <span data-ttu-id="3d848-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d848-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d848-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d848-105">DESCRIPTION</span></span>
<span data-ttu-id="3d848-106">O New-AzContainerRegistry cmdlet cria um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d848-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="3d848-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d848-107">EXAMPLES</span></span>

### <span data-ttu-id="3d848-108">Exemplo 1: Criar um registro de contêiner com uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3d848-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="3d848-109">Este comando cria um registro de contêiner com uma nova conta de armazenamento no grupo de recursos \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="3d848-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="3d848-110">Exemplo 2: Criar um registro de contêiner com o usuário de administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="3d848-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="3d848-111">Este comando cria um registro de contêiner com o usuário de administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="3d848-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="3d848-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d848-112">PARAMETERS</span></span>

### <span data-ttu-id="3d848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d848-113">-DefaultProfile</span></span>
<span data-ttu-id="3d848-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3d848-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d848-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="3d848-115">-EnableAdminUser</span></span>
<span data-ttu-id="3d848-116">Habilitar o usuário de administrador para o registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d848-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="3d848-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3d848-117">-Location</span></span>
<span data-ttu-id="3d848-118">Local do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d848-118">Container Registry Location.</span></span>
<span data-ttu-id="3d848-119">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d848-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="3d848-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d848-120">-Name</span></span>
<span data-ttu-id="3d848-121">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d848-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="3d848-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d848-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d848-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="3d848-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d848-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="3d848-124">-Sku</span></span>
<span data-ttu-id="3d848-125">SKU do Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d848-125">Container Registry SKU.</span></span>
<span data-ttu-id="3d848-126">Valores permitidos: Básico.</span><span class="sxs-lookup"><span data-stu-id="3d848-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="3d848-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d848-127">-Tag</span></span>
<span data-ttu-id="3d848-128">Container Registry Tags.Key-value pairs na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3d848-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="3d848-129">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3d848-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3d848-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d848-130">-Confirm</span></span>
<span data-ttu-id="3d848-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d848-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d848-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d848-132">-WhatIf</span></span>
<span data-ttu-id="3d848-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d848-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d848-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d848-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d848-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d848-135">CommonParameters</span></span>
<span data-ttu-id="3d848-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d848-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d848-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d848-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d848-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d848-138">INPUTS</span></span>

### <span data-ttu-id="3d848-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3d848-139">System.String</span></span>

## <span data-ttu-id="3d848-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d848-140">OUTPUTS</span></span>

### <span data-ttu-id="3d848-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d848-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="3d848-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d848-142">NOTES</span></span>

## <span data-ttu-id="3d848-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d848-143">RELATED LINKS</span></span>

[<span data-ttu-id="3d848-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d848-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="3d848-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d848-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="3d848-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d848-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

