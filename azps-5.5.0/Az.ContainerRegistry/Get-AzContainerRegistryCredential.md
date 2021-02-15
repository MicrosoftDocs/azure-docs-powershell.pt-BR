---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112087"
---
# <span data-ttu-id="92e55-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="92e55-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="92e55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92e55-102">SYNOPSIS</span></span>
<span data-ttu-id="92e55-103">Obtém as credenciais de logon de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="92e55-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="92e55-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92e55-104">SYNTAX</span></span>

### <span data-ttu-id="92e55-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92e55-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e55-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e55-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92e55-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e55-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92e55-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="92e55-108">DESCRIPTION</span></span>
<span data-ttu-id="92e55-109">O Get-AzContainerRegistryCredential cmdlet obtém as credenciais de logon de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="92e55-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="92e55-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92e55-110">EXAMPLES</span></span>

### <span data-ttu-id="92e55-111">Exemplo 1: Obter as credenciais de logon de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="92e55-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="92e55-112">Esse comando obtém as credenciais de logon do registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="92e55-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="92e55-113">O usuário administrador deve estar habilitado para o Registro de \` contêinerEs MyRegistry \` para obter credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="92e55-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="92e55-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92e55-114">PARAMETERS</span></span>

### <span data-ttu-id="92e55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e55-115">-DefaultProfile</span></span>
<span data-ttu-id="92e55-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="92e55-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e55-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="92e55-117">-Name</span></span>
<span data-ttu-id="92e55-118">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="92e55-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="92e55-119">-Registro</span><span class="sxs-lookup"><span data-stu-id="92e55-119">-Registry</span></span>
<span data-ttu-id="92e55-120">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="92e55-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e55-121">-ResourceGroupName</span></span>
<span data-ttu-id="92e55-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e55-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="92e55-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92e55-123">-ResourceId</span></span>
<span data-ttu-id="92e55-124">A ID do recurso de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="92e55-124">The container registry resource id</span></span>

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

### <span data-ttu-id="92e55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e55-125">CommonParameters</span></span>
<span data-ttu-id="92e55-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e55-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92e55-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e55-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="92e55-128">INPUTS</span></span>

### <span data-ttu-id="92e55-129">System.String</span><span class="sxs-lookup"><span data-stu-id="92e55-129">System.String</span></span>

## <span data-ttu-id="92e55-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="92e55-130">OUTPUTS</span></span>

### <span data-ttu-id="92e55-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="92e55-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="92e55-132">Notas</span><span class="sxs-lookup"><span data-stu-id="92e55-132">NOTES</span></span>

## <span data-ttu-id="92e55-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92e55-133">RELATED LINKS</span></span>

[<span data-ttu-id="92e55-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="92e55-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="92e55-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="92e55-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="92e55-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="92e55-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

