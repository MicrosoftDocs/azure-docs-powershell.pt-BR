---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 71eb25c99197513bead7cb400b8a5648c137442d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885924"
---
# <span data-ttu-id="37297-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="37297-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="37297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37297-102">SYNOPSIS</span></span>
<span data-ttu-id="37297-103">Regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="37297-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="37297-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37297-104">SYNTAX</span></span>

### <span data-ttu-id="37297-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="37297-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37297-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37297-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37297-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37297-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37297-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37297-108">DESCRIPTION</span></span>
<span data-ttu-id="37297-109">O Update-AzContainerRegistryCredential cmdlet regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="37297-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="37297-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37297-110">EXAMPLES</span></span>

### <span data-ttu-id="37297-111">Exemplo 1: Regenerar uma credencial de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="37297-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="37297-112">Esse comando regenera uma credencial de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="37297-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="37297-113">O usuário administrador precisa estar habilitado para que o Registro de contêiner \` MyRegistry \` regenere credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="37297-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="37297-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37297-114">PARAMETERS</span></span>

### <span data-ttu-id="37297-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37297-115">-DefaultProfile</span></span>
<span data-ttu-id="37297-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="37297-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37297-117">-Name</span><span class="sxs-lookup"><span data-stu-id="37297-117">-Name</span></span>
<span data-ttu-id="37297-118">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="37297-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37297-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="37297-119">-PasswordName</span></span>
<span data-ttu-id="37297-120">O nome da senha a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="37297-120">The name of password to regenerate.</span></span>
<span data-ttu-id="37297-121">Valores permitidos: senha, senha2.</span><span class="sxs-lookup"><span data-stu-id="37297-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37297-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="37297-122">-Registry</span></span>
<span data-ttu-id="37297-123">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="37297-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37297-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37297-124">-ResourceGroupName</span></span>
<span data-ttu-id="37297-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="37297-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37297-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37297-126">-ResourceId</span></span>
<span data-ttu-id="37297-127">A ID de recurso do Registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="37297-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37297-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37297-128">-Confirm</span></span>
<span data-ttu-id="37297-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37297-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37297-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37297-130">-WhatIf</span></span>
<span data-ttu-id="37297-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37297-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37297-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37297-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37297-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37297-133">CommonParameters</span></span>
<span data-ttu-id="37297-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37297-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37297-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37297-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37297-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37297-136">INPUTS</span></span>

### <span data-ttu-id="37297-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37297-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="37297-138">System.String</span><span class="sxs-lookup"><span data-stu-id="37297-138">System.String</span></span>

## <span data-ttu-id="37297-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37297-139">OUTPUTS</span></span>

### <span data-ttu-id="37297-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="37297-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="37297-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="37297-141">NOTES</span></span>

## <span data-ttu-id="37297-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37297-142">RELATED LINKS</span></span>

[<span data-ttu-id="37297-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37297-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="37297-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37297-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="37297-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="37297-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

