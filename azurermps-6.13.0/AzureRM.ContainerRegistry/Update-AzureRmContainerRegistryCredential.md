---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440807"
---
# <span data-ttu-id="084cc-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="084cc-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="084cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="084cc-102">SYNOPSIS</span></span>
<span data-ttu-id="084cc-103">Regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="084cc-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="084cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="084cc-104">SYNTAX</span></span>

### <span data-ttu-id="084cc-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="084cc-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="084cc-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="084cc-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="084cc-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="084cc-108">DESCRIPTION</span></span>
<span data-ttu-id="084cc-109">O cmdlet Update-AzureRmContainerRegistryCredential regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="084cc-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="084cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="084cc-110">EXAMPLES</span></span>

### <span data-ttu-id="084cc-111">Exemplo 1: regenerar uma credencial de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="084cc-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="084cc-112">Esse comando regenera uma credencial de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="084cc-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="084cc-113">O usuário administrador precisa estar habilitado para o meu \` registro do contêiner \` para gerar novamente as credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="084cc-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="084cc-114">OS</span><span class="sxs-lookup"><span data-stu-id="084cc-114">PARAMETERS</span></span>

### <span data-ttu-id="084cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084cc-115">-DefaultProfile</span></span>
<span data-ttu-id="084cc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="084cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="084cc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="084cc-117">-Name</span></span>
<span data-ttu-id="084cc-118">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="084cc-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="084cc-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="084cc-119">-PasswordName</span></span>
<span data-ttu-id="084cc-120">O nome da senha para gerar novamente.</span><span class="sxs-lookup"><span data-stu-id="084cc-120">The name of password to regenerate.</span></span>
<span data-ttu-id="084cc-121">Valores permitidos: password, password2.</span><span class="sxs-lookup"><span data-stu-id="084cc-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="084cc-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="084cc-122">-Registry</span></span>
<span data-ttu-id="084cc-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="084cc-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="084cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="084cc-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="084cc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="084cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="084cc-126">-ResourceId</span></span>
<span data-ttu-id="084cc-127">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="084cc-127">The container registry resource id</span></span>

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

### <span data-ttu-id="084cc-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="084cc-128">-Confirm</span></span>
<span data-ttu-id="084cc-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084cc-130">-WhatIf</span></span>
<span data-ttu-id="084cc-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="084cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084cc-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="084cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084cc-133">CommonParameters</span></span>
<span data-ttu-id="084cc-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084cc-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084cc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084cc-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="084cc-136">INPUTS</span></span>

### <span data-ttu-id="084cc-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="084cc-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="084cc-138">Parâmetros: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="084cc-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="084cc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="084cc-139">System.String</span></span>

## <span data-ttu-id="084cc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="084cc-140">OUTPUTS</span></span>

### <span data-ttu-id="084cc-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="084cc-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="084cc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="084cc-142">NOTES</span></span>

## <span data-ttu-id="084cc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="084cc-143">RELATED LINKS</span></span>

[<span data-ttu-id="084cc-144">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="084cc-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="084cc-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="084cc-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="084cc-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="084cc-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

