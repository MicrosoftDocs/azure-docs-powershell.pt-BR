---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115590"
---
# <span data-ttu-id="f655e-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f655e-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="f655e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f655e-102">SYNOPSIS</span></span>
<span data-ttu-id="f655e-103">Faça logon em um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="f655e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f655e-104">SYNTAX</span></span>

### <span data-ttu-id="f655e-105">WithoutNameAndPasswordParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f655e-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f655e-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="f655e-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f655e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f655e-107">DESCRIPTION</span></span>
<span data-ttu-id="f655e-108">Faça logon em um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="f655e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f655e-109">EXAMPLES</span></span>

### <span data-ttu-id="f655e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f655e-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="f655e-111">Faça logon em ACR sem credenciais quando já se conectar à conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="f655e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f655e-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="f655e-113">Faça logon em ACR com nome de usuário/senha de administrador quando o usuário administrador estava habilitado.</span><span class="sxs-lookup"><span data-stu-id="f655e-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="f655e-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f655e-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="f655e-115">Faça logon em ACR com a ID de aplicativo e a senha do serviço principal.</span><span class="sxs-lookup"><span data-stu-id="f655e-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="f655e-116">OS</span><span class="sxs-lookup"><span data-stu-id="f655e-116">PARAMETERS</span></span>

### <span data-ttu-id="f655e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f655e-117">-DefaultProfile</span></span>
<span data-ttu-id="f655e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f655e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f655e-119">-Name</span></span>
<span data-ttu-id="f655e-120">Nome do registro do contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f655e-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="f655e-121">-Password</span></span>
<span data-ttu-id="f655e-122">Senha do registro do contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f655e-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="f655e-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="f655e-123">-UserName</span></span>
<span data-ttu-id="f655e-124">Nome de usuário do registro do Azure container.</span><span class="sxs-lookup"><span data-stu-id="f655e-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="f655e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f655e-125">CommonParameters</span></span>
<span data-ttu-id="f655e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f655e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f655e-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f655e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f655e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f655e-128">INPUTS</span></span>

### <span data-ttu-id="f655e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f655e-129">System.String</span></span>

## <span data-ttu-id="f655e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f655e-130">OUTPUTS</span></span>

### <span data-ttu-id="f655e-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f655e-131">System.Boolean</span></span>

## <span data-ttu-id="f655e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f655e-132">NOTES</span></span>

## <span data-ttu-id="f655e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f655e-133">RELATED LINKS</span></span>
