---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264105"
---
# <span data-ttu-id="429aa-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="429aa-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="429aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="429aa-102">SYNOPSIS</span></span>
<span data-ttu-id="429aa-103">Regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="429aa-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="429aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="429aa-104">SYNTAX</span></span>

### <span data-ttu-id="429aa-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="429aa-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="429aa-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="429aa-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="429aa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="429aa-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="429aa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="429aa-108">DESCRIPTION</span></span>
<span data-ttu-id="429aa-109">O cmdlet Update-AzContainerRegistryCredential regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="429aa-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="429aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="429aa-110">EXAMPLES</span></span>

### <span data-ttu-id="429aa-111">Exemplo 1: regenerar uma credencial de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="429aa-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="429aa-112">Esse comando regenera uma credencial de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="429aa-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="429aa-113">O usuário administrador precisa estar habilitado para o meu \` registro do contêiner \` para gerar novamente as credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="429aa-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="429aa-114">OS</span><span class="sxs-lookup"><span data-stu-id="429aa-114">PARAMETERS</span></span>

### <span data-ttu-id="429aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429aa-115">-DefaultProfile</span></span>
<span data-ttu-id="429aa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="429aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="429aa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="429aa-117">-Name</span></span>
<span data-ttu-id="429aa-118">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="429aa-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="429aa-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="429aa-119">-PasswordName</span></span>
<span data-ttu-id="429aa-120">O nome da senha para gerar novamente.</span><span class="sxs-lookup"><span data-stu-id="429aa-120">The name of password to regenerate.</span></span>
<span data-ttu-id="429aa-121">Valores permitidos: password, password2.</span><span class="sxs-lookup"><span data-stu-id="429aa-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="429aa-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="429aa-122">-Registry</span></span>
<span data-ttu-id="429aa-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="429aa-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="429aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="429aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="429aa-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="429aa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="429aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="429aa-126">-ResourceId</span></span>
<span data-ttu-id="429aa-127">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="429aa-127">The container registry resource id</span></span>

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

### <span data-ttu-id="429aa-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="429aa-128">-Confirm</span></span>
<span data-ttu-id="429aa-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="429aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="429aa-130">-WhatIf</span></span>
<span data-ttu-id="429aa-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="429aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="429aa-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="429aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="429aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429aa-133">CommonParameters</span></span>
<span data-ttu-id="429aa-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429aa-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="429aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429aa-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="429aa-136">INPUTS</span></span>

### <span data-ttu-id="429aa-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="429aa-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="429aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="429aa-138">System.String</span></span>

## <span data-ttu-id="429aa-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="429aa-139">OUTPUTS</span></span>

### <span data-ttu-id="429aa-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="429aa-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="429aa-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="429aa-141">NOTES</span></span>

## <span data-ttu-id="429aa-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="429aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="429aa-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="429aa-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="429aa-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="429aa-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="429aa-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="429aa-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

