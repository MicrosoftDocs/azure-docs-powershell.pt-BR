---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: be045303db770cbba919d27ed9563aa64283572c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892209"
---
# <span data-ttu-id="55fad-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="55fad-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="55fad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55fad-102">SYNOPSIS</span></span>
<span data-ttu-id="55fad-103">Faça logon em um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="55fad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55fad-104">SYNTAX</span></span>

### <span data-ttu-id="55fad-105">WithoutNameAndPasswordParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="55fad-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55fad-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="55fad-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55fad-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55fad-107">DESCRIPTION</span></span>
<span data-ttu-id="55fad-108">Faça logon em um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="55fad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55fad-109">EXAMPLES</span></span>

### <span data-ttu-id="55fad-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55fad-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="55fad-111">Faça logon no ACR sem credenciais quando já entrar na conta do azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="55fad-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="55fad-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="55fad-113">Faça logon no ACR com nome de usuário/senha do administrador quando o usuário do administrador estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="55fad-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="55fad-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="55fad-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="55fad-115">Faça logon no ACR com a ID do aplicativo principal de serviço e a senha.</span><span class="sxs-lookup"><span data-stu-id="55fad-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="55fad-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55fad-116">PARAMETERS</span></span>

### <span data-ttu-id="55fad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fad-117">-DefaultProfile</span></span>
<span data-ttu-id="55fad-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55fad-119">-Name</span><span class="sxs-lookup"><span data-stu-id="55fad-119">-Name</span></span>
<span data-ttu-id="55fad-120">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fad-121">-Password</span><span class="sxs-lookup"><span data-stu-id="55fad-121">-Password</span></span>
<span data-ttu-id="55fad-122">Senha para o Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fad-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="55fad-123">-UserName</span></span>
<span data-ttu-id="55fad-124">Nome de usuário do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="55fad-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fad-125">CommonParameters</span></span>
<span data-ttu-id="55fad-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fad-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55fad-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fad-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55fad-128">INPUTS</span></span>

### <span data-ttu-id="55fad-129">System.String</span><span class="sxs-lookup"><span data-stu-id="55fad-129">System.String</span></span>

## <span data-ttu-id="55fad-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55fad-130">OUTPUTS</span></span>

### <span data-ttu-id="55fad-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55fad-131">System.Boolean</span></span>

## <span data-ttu-id="55fad-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="55fad-132">NOTES</span></span>

## <span data-ttu-id="55fad-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55fad-133">RELATED LINKS</span></span>
