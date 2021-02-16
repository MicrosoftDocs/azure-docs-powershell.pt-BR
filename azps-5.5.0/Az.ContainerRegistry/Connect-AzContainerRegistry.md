---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 3c702d0572bb8e5bdf41deff599b9da6c5cc2dcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127056"
---
# <span data-ttu-id="3ef04-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ef04-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="3ef04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ef04-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef04-103">Faça logon em um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="3ef04-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ef04-104">SYNTAX</span></span>

### <span data-ttu-id="3ef04-105">SemNameAndPasswordParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ef04-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ef04-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ef04-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ef04-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ef04-107">DESCRIPTION</span></span>
<span data-ttu-id="3ef04-108">Faça logon em um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="3ef04-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ef04-109">EXAMPLES</span></span>

### <span data-ttu-id="3ef04-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ef04-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="3ef04-111">Faça logon no ACR sem credenciais quando já estiver em uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="3ef04-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3ef04-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="3ef04-113">Faça logon no ACR com nome de usuário/senha do administrador quando o usuário administrador foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="3ef04-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="3ef04-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3ef04-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="3ef04-115">Faça logon no ACR com a ID e a senha do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="3ef04-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="3ef04-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ef04-116">PARAMETERS</span></span>

### <span data-ttu-id="3ef04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef04-117">-DefaultProfile</span></span>
<span data-ttu-id="3ef04-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef04-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ef04-119">-Name</span></span>
<span data-ttu-id="3ef04-120">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="3ef04-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="3ef04-121">-Password</span></span>
<span data-ttu-id="3ef04-122">Senha do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="3ef04-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="3ef04-123">-UserName</span></span>
<span data-ttu-id="3ef04-124">Nome de Usuário do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef04-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="3ef04-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef04-125">CommonParameters</span></span>
<span data-ttu-id="3ef04-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef04-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef04-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ef04-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef04-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ef04-128">INPUTS</span></span>

### <span data-ttu-id="3ef04-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3ef04-129">System.String</span></span>

## <span data-ttu-id="3ef04-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ef04-130">OUTPUTS</span></span>

### <span data-ttu-id="3ef04-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ef04-131">System.Boolean</span></span>

## <span data-ttu-id="3ef04-132">Notas</span><span class="sxs-lookup"><span data-stu-id="3ef04-132">NOTES</span></span>

## <span data-ttu-id="3ef04-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ef04-133">RELATED LINKS</span></span>
