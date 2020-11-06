---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426399"
---
# <span data-ttu-id="d4e71-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d4e71-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="d4e71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4e71-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e71-103">Obtém as credenciais de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="d4e71-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4e71-104">SYNTAX</span></span>

### <span data-ttu-id="d4e71-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d4e71-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4e71-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4e71-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4e71-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4e71-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4e71-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4e71-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e71-109">O cmdlet Get-AzureRmContainerRegistryCredential Obtém as credenciais de logon para um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d4e71-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="d4e71-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4e71-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e71-111">Exemplo 1: obter as credenciais de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="d4e71-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="d4e71-112">Este comando obtém as credenciais de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="d4e71-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="d4e71-113">O usuário administrador precisa estar habilitado para o meu \` registro do contêiner \` para obter as credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="d4e71-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="d4e71-114">OS</span><span class="sxs-lookup"><span data-stu-id="d4e71-114">PARAMETERS</span></span>

### <span data-ttu-id="d4e71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e71-115">-DefaultProfile</span></span>
<span data-ttu-id="d4e71-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d4e71-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e71-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4e71-117">-Name</span></span>
<span data-ttu-id="d4e71-118">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d4e71-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="d4e71-119">-Registro</span><span class="sxs-lookup"><span data-stu-id="d4e71-119">-Registry</span></span>
<span data-ttu-id="d4e71-120">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d4e71-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="d4e71-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e71-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4e71-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4e71-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4e71-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e71-123">-ResourceId</span></span>
<span data-ttu-id="d4e71-124">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="d4e71-124">The container registry resource id</span></span>

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

### <span data-ttu-id="d4e71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e71-125">CommonParameters</span></span>
<span data-ttu-id="d4e71-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e71-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e71-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e71-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4e71-128">INPUTS</span></span>

### <span data-ttu-id="d4e71-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e71-129">System.String</span></span>

## <span data-ttu-id="d4e71-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4e71-130">OUTPUTS</span></span>

### <span data-ttu-id="d4e71-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d4e71-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="d4e71-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4e71-132">NOTES</span></span>

## <span data-ttu-id="d4e71-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4e71-133">RELATED LINKS</span></span>

[<span data-ttu-id="d4e71-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4e71-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="d4e71-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4e71-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="d4e71-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d4e71-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)
