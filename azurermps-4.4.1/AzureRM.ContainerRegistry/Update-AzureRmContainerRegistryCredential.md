---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602707"
---
# <span data-ttu-id="fb863-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fb863-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="fb863-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb863-102">SYNOPSIS</span></span>
<span data-ttu-id="fb863-103">Regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="fb863-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb863-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb863-104">SYNTAX</span></span>

### <span data-ttu-id="fb863-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb863-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb863-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb863-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb863-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb863-107">DESCRIPTION</span></span>
<span data-ttu-id="fb863-108">O cmdlet **Update-AzureRmContainerRegistryCredential** regenera uma credencial de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="fb863-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="fb863-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb863-109">EXAMPLES</span></span>

### <span data-ttu-id="fb863-110">Exemplo 1: regenerar uma credencial de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="fb863-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="fb863-111">Esse comando regenera uma credencial de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="fb863-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="fb863-112">O usuário administrador precisa estar habilitado para o registro do contêiner `MyRegistry` gerar novamente as credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="fb863-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="fb863-113">OS</span><span class="sxs-lookup"><span data-stu-id="fb863-113">PARAMETERS</span></span>

### <span data-ttu-id="fb863-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb863-114">-Name</span></span>
<span data-ttu-id="fb863-115">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fb863-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="fb863-116">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="fb863-116">-PasswordName</span></span>
<span data-ttu-id="fb863-117">O nome da senha para gerar novamente.</span><span class="sxs-lookup"><span data-stu-id="fb863-117">The name of password to regenerate.</span></span>
<span data-ttu-id="fb863-118">Valores permitidos: password, password2.</span><span class="sxs-lookup"><span data-stu-id="fb863-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb863-119">-Registro</span><span class="sxs-lookup"><span data-stu-id="fb863-119">-Registry</span></span>
<span data-ttu-id="fb863-120">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fb863-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="fb863-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb863-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb863-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb863-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb863-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb863-123">-Confirm</span></span>
<span data-ttu-id="fb863-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb863-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb863-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb863-125">-WhatIf</span></span>
<span data-ttu-id="fb863-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb863-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb863-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb863-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb863-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb863-128">-DefaultProfile</span></span>
<span data-ttu-id="fb863-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb863-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb863-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb863-130">CommonParameters</span></span>
<span data-ttu-id="fb863-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb863-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb863-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb863-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb863-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb863-133">INPUTS</span></span>

### <span data-ttu-id="fb863-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb863-134">PSContainerRegistry</span></span>
<span data-ttu-id="fb863-135">O parâmetro ' Registry ' aceita o valor do tipo ' PSContainerRegistry ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="fb863-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="fb863-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb863-136">OUTPUTS</span></span>

### <span data-ttu-id="fb863-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fb863-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="fb863-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb863-138">NOTES</span></span>

## <span data-ttu-id="fb863-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb863-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb863-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb863-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="fb863-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb863-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="fb863-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fb863-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

