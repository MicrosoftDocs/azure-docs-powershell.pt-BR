---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112081"
---
# <span data-ttu-id="775d6-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="775d6-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="775d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="775d6-102">SYNOPSIS</span></span>
<span data-ttu-id="775d6-103">Cria um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="775d6-103">Creates a container registry.</span></span>

## <span data-ttu-id="775d6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="775d6-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="775d6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="775d6-105">DESCRIPTION</span></span>
<span data-ttu-id="775d6-106">O New-AzContainerRegistry cmdlet cria um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="775d6-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="775d6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="775d6-107">EXAMPLES</span></span>

### <span data-ttu-id="775d6-108">Exemplo 1: Criar um registro de contêiner com uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="775d6-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="775d6-109">Esse comando cria um registro de contêiner com uma nova conta de armazenamento no grupo de recursos \` MyResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="775d6-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="775d6-110">Exemplo 2: Criar um registro de contêiner com o usuário de administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="775d6-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="775d6-111">Esse comando cria um registro de contêiner com o usuário de administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="775d6-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="775d6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="775d6-112">PARAMETERS</span></span>

### <span data-ttu-id="775d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775d6-113">-DefaultProfile</span></span>
<span data-ttu-id="775d6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="775d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="775d6-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="775d6-115">-EnableAdminUser</span></span>
<span data-ttu-id="775d6-116">Habilitar o usuário administrador para o registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="775d6-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="775d6-117">-Local</span><span class="sxs-lookup"><span data-stu-id="775d6-117">-Location</span></span>
<span data-ttu-id="775d6-118">Local do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="775d6-118">Container Registry Location.</span></span>
<span data-ttu-id="775d6-119">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="775d6-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="775d6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="775d6-120">-Name</span></span>
<span data-ttu-id="775d6-121">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="775d6-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="775d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="775d6-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="775d6-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="775d6-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="775d6-124">-Sku</span></span>
<span data-ttu-id="775d6-125">SKU do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="775d6-125">Container Registry SKU.</span></span>
<span data-ttu-id="775d6-126">Valores permitidos: Básico.</span><span class="sxs-lookup"><span data-stu-id="775d6-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="775d6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="775d6-127">-Tag</span></span>
<span data-ttu-id="775d6-128">Container Registry Tags.Key-value pairs na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="775d6-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="775d6-129">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="775d6-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="775d6-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="775d6-130">-Confirm</span></span>
<span data-ttu-id="775d6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="775d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="775d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="775d6-132">-WhatIf</span></span>
<span data-ttu-id="775d6-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="775d6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="775d6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="775d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="775d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775d6-135">CommonParameters</span></span>
<span data-ttu-id="775d6-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775d6-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="775d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775d6-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="775d6-138">INPUTS</span></span>

### <span data-ttu-id="775d6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="775d6-139">System.String</span></span>

## <span data-ttu-id="775d6-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="775d6-140">OUTPUTS</span></span>

### <span data-ttu-id="775d6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="775d6-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="775d6-142">Notas</span><span class="sxs-lookup"><span data-stu-id="775d6-142">NOTES</span></span>

## <span data-ttu-id="775d6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="775d6-143">RELATED LINKS</span></span>

[<span data-ttu-id="775d6-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="775d6-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="775d6-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="775d6-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="775d6-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="775d6-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

