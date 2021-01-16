---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261247"
---
# <span data-ttu-id="039e3-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="039e3-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="039e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="039e3-102">SYNOPSIS</span></span>
<span data-ttu-id="039e3-103">Obtém as credenciais de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="039e3-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="039e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="039e3-104">SYNTAX</span></span>

### <span data-ttu-id="039e3-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="039e3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="039e3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="039e3-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="039e3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="039e3-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="039e3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="039e3-108">DESCRIPTION</span></span>
<span data-ttu-id="039e3-109">O cmdlet Get-AzContainerRegistryCredential Obtém as credenciais de logon para um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="039e3-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="039e3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="039e3-110">EXAMPLES</span></span>

### <span data-ttu-id="039e3-111">Exemplo 1: obter as credenciais de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="039e3-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="039e3-112">Este comando obtém as credenciais de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="039e3-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="039e3-113">O usuário administrador precisa estar habilitado para o meu \` registro do contêiner \` para obter as credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="039e3-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="039e3-114">OS</span><span class="sxs-lookup"><span data-stu-id="039e3-114">PARAMETERS</span></span>

### <span data-ttu-id="039e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039e3-115">-DefaultProfile</span></span>
<span data-ttu-id="039e3-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="039e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="039e3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="039e3-117">-Name</span></span>
<span data-ttu-id="039e3-118">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="039e3-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="039e3-119">-Registro</span><span class="sxs-lookup"><span data-stu-id="039e3-119">-Registry</span></span>
<span data-ttu-id="039e3-120">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="039e3-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="039e3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039e3-121">-ResourceGroupName</span></span>
<span data-ttu-id="039e3-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="039e3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="039e3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="039e3-123">-ResourceId</span></span>
<span data-ttu-id="039e3-124">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="039e3-124">The container registry resource id</span></span>

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

### <span data-ttu-id="039e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039e3-125">CommonParameters</span></span>
<span data-ttu-id="039e3-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039e3-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="039e3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039e3-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="039e3-128">INPUTS</span></span>

### <span data-ttu-id="039e3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="039e3-129">System.String</span></span>

## <span data-ttu-id="039e3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="039e3-130">OUTPUTS</span></span>

### <span data-ttu-id="039e3-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="039e3-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="039e3-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="039e3-132">NOTES</span></span>

## <span data-ttu-id="039e3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="039e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="039e3-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="039e3-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="039e3-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="039e3-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="039e3-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="039e3-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

